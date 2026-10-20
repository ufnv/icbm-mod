# 14 — Explodopedia

[Index](index.md) · [Technologies](05-Technologies.md) · [Tech modifiers](06-Tech-Modifiers.md) · [Other configuration files](12-Config-Files.md)

The Explodopedia is the game's encyclopedia, opened from the main menu. Almost all of it is built from the
data files when it opens: every unit, weapon, sensor, research and nuclear explosion of the game and of the
loaded mods gets its page, with its values, upgrades and counters. A mod's units, weapons and research
appear there without any extra work. Only the descriptions of the categories and the articles of the
general information tab are written by hand, in `Lang/<language>/explodopedia.lng`.

Contents

1. [The tabs and what appears in them](#1-the-tabs-and-what-appears-in-them)
2. [What a page shows, and where it comes from](#2-what-a-page-shows-and-where-it-comes-from)
3. [explodopedia.lng](#3-explodopedialng)
4. [General information articles](#4-general-information-articles)
5. [Articles in HTML](#5-articles-in-html)
6. [Step by step: adding an HTML article](#6-step-by-step-adding-an-html-article)
7. [Mods and translations](#7-mods-and-translations)
8. [Pitfalls](#8-pitfalls)

---

## 1. The tabs and what appears in them

| Tab | One page per | Categories (the icons above the list) | Left out |
|---|---|---|---|
| **Units** | unit technology (the modes of a unit, such as a surfaced submarine, share one page) | the unit classes, `[UNIT_CLASS]` in `tech.txt` ([05](05-Technologies.md)), in their order, as on the production screen; units without a class get a category of their own | `VirtualCity`, special states, virtual missile units, cities, abstract positions |
| **Weapons** | missile (`[MISSILE]`) | Nuclear weapons (nuclear, or carrying a nuclear warhead); Chemical and biological weapons (special); Air and missile defence (usable only against aircraft and missiles); Naval weapons (only against ships and submarines); Anti-satellite weapons (only against satellites); Conventional strike weapons (the rest) | `Hidden` missiles; MIRV warheads that no unit carries on their own |
| **Radars** | radar (`[RADAR]`) | Underwater detection (detects submarines); Air and missile detection; Space detection (only satellites); Surface detection (the rest); the game's `Explodopedia.txt` adds Optical sensors and Satellite cameras and sorts the radars by rules ([§3](#explodopediatxt-icons-and-the-start-page)) | radars with `DoNotShow` (the plain vision) |
| **Research** | research technology | the research fields (`[TYPE]`); a field's overview draws its research tree as the research screen does | — |
| **Explosions** | nuclear explosion yield | one category | explosions that no listed weapon delivers; explosions with no `Kilotons` |
| **General** | article in `explodopedia.lng` | first **Gameplay hints**: the hints of the loading screens (`loading.lng`, [12 §5](12-Config-Files.md#5-language-files)) as a numbered list; then the chapters of the articles | — |

An object gets a page only when **its technology has a name** in `tech_t.lng` (or the mod's own language
file). A unit, weapon or radar without a named technology does not appear.

**Keeping an object out**: `DoNotShowInEncyclopedia` (or its alias `DoNotShowInExplodopedia`) in a
`[UNIT]`, `[MISSILE]`, `[RADAR]` or `[EXPLOSION]` keeps it out of the Explodopedia entirely: it has no page,
and no other page mentions it: not as an icon (weapons, radars, platforms, the units with a trait, the weapons
of an aura), not as a link (replaced by, delivered by), and not by its technology's name in the counters. A
weapon's MIRV warheads go with it. Write it bare (= Yes) or with `Yes`/`No`; it is not inherited from a
`[TYPE]`, and a `Type` line after it does not clear it.

```
[UNIT] "Test_Dummy"
  Tech "U_Test_Dummy"
  DoNotShowInEncyclopedia
```

Several radars of the same technology share its name; the second and later ones get their ID added in
brackets.

## 2. What a page shows, and where it comes from

**Name and description**: the technology's name and description from `tech_t.lng`. A technology whose
description is missing (the text shown is its key) gets no description.

**Picture**: a unit's icon and 3D model; a weapon's picture (`Image`). Upgrades that change the look
(`ImprovedBy "Tech" Movie Image "…"`, a new model) give the page levels: the arrows under the picture step
through them, and the values, upgrades and counters on the page follow the level shown.

**Values**: hit points, speed, ranges, yield, warheads, hit spread, interception chance, production cost
and the others, read from the data with the upgrades of the level shown already applied. A value changed
by the level is green.

**Upgrades** (`ImprovedBy` with a research, [06](06-Tech-Modifiers.md)): each research, with what it changes,
e.g. "Speed +10%, Hit points 1.2". A modifier with a helper technology (a `_Buffer` technology that only a
research gives) is listed under that research. A unit's `Size` change of 2% or less is not shown: such
changes are markers for other modifiers, not real size changes. When a research gives the unit a trait
(a `Modifier` tag) that enemy weapons or radars react to (their `AffectedBy Unit "Tag"`), the research row
also tells what that does: "Enemy weapons against it: Hit spread +7.5%, Damage −10%". When the weapons are
affected differently, a row each lists the weapons as icons.

**Improved by, in a situation**: `ImprovedBy Unit "Tag"` (better when carried by or launched from units with
the tag; the units shown as icons) and `ImprovedBy InRange "Weapon"` (inside the aura of a weapon).

**Countered by** (`AffectedBy`):

| Group | From | Shown as |
|---|---|---|
| Enemy research | `AffectedBy "Tech"` (global), and `AffectedBy Unit "Tag"` when a research gives the tag | the research, a link |
| Enemy traits | `AffectedBy Unit "Tag"` | the tag's effect and the units that carry it, as icons with their names as tooltips; a tag that the cities carry (the DEFCON levels) keeps its name and shows the city |
| In range of | `AffectedBy InRange "Weapon"` | the aura's weapons, as icons |
| After an explosion of | `AffectedBy Explosion "Explosion"` | the weapon that delivers it |
| On terrain | `AffectedBy Terrain "Terrain"` | the terrain |

A `Complex` modifier whose cases are all `Case Self "Tech"` (the effect depends on the weapon's own
research, e.g. the accuracy penalties of ballistic missiles) is shown with the effect of the level shown.

**Weapons only**: the platforms (the units whose weapon configurations carry it, with the research a
configuration needs), the explosion it delivers, **Replaces / Replaced by** (a weapon in the same category
made obsolete by the research that unlocks the other one) and **Made obsolete by** (the research that ends
its production: its `DisablingTech`, or an `ImprovedBy "Tech" CanBeBuilt 0`). A missile with
`CanBeIntercepted` above 0 ends its page with **Can be intercepted by** (UI 2594, after the platforms): the weapons with a platform that can
be fired at it (`CanBeUsedAgainst` its `Missile` / `HighMissile` type), as icons, without the interceptor
classes its `DisableCanBeIntercepted` excludes ([02](02-Missiles.md)).

**Units only**: weapons, radars, the units it carries and where it is based.

**Research only**: what it unlocks, improves and makes obsolete, what it needs and what it leads to.

**Nuclear explosions**: one page per yield, with its burst variants (ground, water, air, space;
[03](03-Explosions.md)) and the weapons that deliver it. Each explosion fills its frame; the marks behind it
tell its size, and their brightness legend is the same for every yield (a 1 kt burst has its
marks almost alike, a 100 Mt one the whole range).

## 3. explodopedia.lng

`Lang/<language>/explodopedia.lng` holds the hand-written texts, in the form of `unit.lng`:

```
"KEY" LANG "text"
```

`\n` in a text is a new line, `\"` a quote. `USE` and `IF` work as in the other language files
([12 §5](12-Config-Files.md#5-language-files)). The English file is read first and the language's file over
it: a key missing in a language shows the English text.

| Key | Text |
|---|---|
| `CATEGORY_<class ID>` | a unit category's overview: the ID of its `[UNIT_CLASS]`, e.g. `CATEGORY_UC_Naval` |
| `CATEGORY_Classless` | the category of the units without a class |
| `CATEGORY_Nuclear`, `_ChemBio`, `_Defence`, `_Naval`, `_Conventional`, `_AntiSat` | the weapon categories |
| `CATEGORY_RadarAir`, `_RadarSurface`, `_RadarUnderwater`, `_RadarSpace` | the radar categories |
| `CATEGORY_Explosions` | the explosions tab |
| `CATEGORY_PLACEHOLDER` | a category without its own text; `%s` is the category's name |
| `FIELD_<[TYPE] ID>` | a research field's overview, e.g. `"FIELD_Weapons of Mass Destruction"` |
| `FIELD_PLACEHOLDER` | a field without its own text |
| `EXPLOSION_<[EXPLOSION] ID>` | a nuclear explosion's page, by any explosion of its yield, e.g. `EXPLOSION_nuke_1000` for 1 Mt |
| `EXPLOSION_PLACEHOLDER` | an explosion without its own text |
| `HINTS_DESC` | optional: a text above the gameplay hints |
| `GENERAL_…` | the general information tab ([§4](#4-general-information-articles)) |

### Explodopedia.txt: icons and the start page

The icons of the tabs and the categories, and the page the Explodopedia opens on, are not a language's: they
are set in `Explodopedia.txt` in the game's folder. A mod changes it with its own `Explodopedia.txt` starting
with `USE PREVIOUS "Explodopedia.txt"`; `IF` works as in the other files.

```
Tab "Research" Icon "Overlay_Science"
Category "FIELD_Weapons of Mass Destruction" Icon "Nuclear_Fission"
Category "FIELD_Radar Systems" Icon "Radar_Mk2"
Category "CATEGORY_UC_Naval" Icon "Images/Explodopedia/naval.png" Scale 1.2
StartPage "GENERAL_1"
```

| Line | Meaning |
|---|---|
| `Tab "<name>" [Icon "<icon>"] [Scale <f>] [Hide]` | a tab's icon; the names: `Units`, `Weapons`, `Radars`, `Research`, `Explosions`, `General` |
| `Category "<key>" [Icon "<icon>"] [Scale <f>] [Hide]` | a category's icon above the list (without one: the picture of its first page). The key: `FIELD_<[TYPE] ID>` (a research field), `CATEGORY_<[UNIT_CLASS] ID>` (a unit class), `CATEGORY_Nuclear` … `CATEGORY_AntiSat` (the weapons), `CATEGORY_RadarAir` … `CATEGORY_RadarSpace`, `CATEGORY_Explosions`, `GENERAL_<c>` (an article chapter), `HINTS` (the gameplay hints) |
| `NewCategory "<key>" Tab "<tab>" [After "<category key>"] [Icon …] [Scale …] [Hide]` | a category of its own in a tab, after the category named (else last). Its name is `<key>_NAME` and its description `<key>` in `explodopedia.lng`, so it is translated with the other texts |
| `Category "<key>" After "<category key>"` | a category moved after another of its tab |
| `Tab "<tab>" Auto No` | none of the game's categories in that tab: its pages only where the rules put them (into `NewCategory` ones), the others left out |
| `Put <kind> [Where <test> [And <test>]…] In "<category key>"` | a rule: the pages of a kind (`Units`, `Weapons`, `Radars`, `Research`, `Explosions`) that pass all the tests into that category |
| `Exclude <kind> [Where <test> [And <test>]…]` | a rule: those pages left out of the Explodopedia |
| `Put "<page>" In "<category key>"` | one page (its ID or name, as an article's link) in that category, over all the rules |
| `HideProperty <property>… Of <kind> [Where <test> [And <test>]…]` | those properties (named as in the data files: `Speed`, `Damage`, `Range`, `Precision`, `CanBeIntercepted`…) not shown on the pages selected: no value row, no change in their upgrades and counters |
| `HideModifier "<source>"… Of <kind> [Where <test> [And <test>]…]` | every effect from those sources (the ID of a technology or trait, an explosion, an aura's weapon; `*` any characters) left out of the upgrades and counters of the pages selected |
| `StartPage "<page or key>"` | what it opens on: a page (its ID or name, as an article's link) or a category's overview (its key). Without it: the general tab's first category |

An icon is, in this order: a UI element, by its name in `UI/UI.txt` (`"Main_Button_Globe"`) or its number; a
page of the Explodopedia, its picture (the ID or the name of a unit, weapon, radar, research or explosion); or a
picture file, its path from the game's folder (a mod's own pictures from the mod's folder). `Scale` draws it
that much larger, for an icon with wide empty margins. An icon that is not found leaves the default one and writes a warning to `Fatal.txt`.

Without these lines the categories are the game's: units by their `[UNIT_CLASS]`, research by its field, weapons
and radars by rules on what they hit or detect, explosions in one (§1). The rules go in the order of the lines, a
later one over an earlier one; a page no rule matches stays where the game put it. A test, with `Not` before it for
its opposite (`*` in a text: any characters):

| Test | Pages | Passes when |
|---|---|---|
| `ID "<pattern>"`, `Name "<pattern>"`, `Tech "<pattern>"` | any | its ID, its name as shown, its technology's ID match |
| `Level [Min <n>] [Max <n>]` | any | the research level it needs (a research: its own) is in the range |
| `UnitType <unit types>` | units | its type is one of them (`Ground`, `Naval`, `Subwater`, `Airborne`, `Missile`, `HighMissile`, `SubwaterMissile`, `Satellite`) |
| `Class "<[UNIT_CLASS] ID>"` | units, weapons | its class (a weapon's: its `Class` line in Missile_defs.txt) |
| `Geneva "<category>"` (or `GenevaCategory`) | weapons | it is in a treaties' category the pattern matches (its `GenevaCategory` lines, e.g. `"Salted Weapons"`, `"EMP Weapons"`) |
| `Against <unit types>`, `OnlyAgainst <unit types>`, `Nuclear`, `ChemBio`, `Kilotons [Min <n>] [Max <n>]` | weapons | it can be used against one of them; only against them (and something); a nuclear yield (EMP ones too); chemical or biological; its total yield |
| `ShowType <range layer>`, `Detects <unit types>`, `DetectsNothing` | radars | its `GlobalShowType` (`SW_RANGES`, `LW_RANGES`, `OVERHORIZONT_RANGES`, `SONAR_RANGES`, `SPACE_RANGES`, `SATELLITE_RANGES`, `OPTICAL_RANGES`); what it detects |
| `Field "<[TYPE] ID>"` | research | its field |
| `Kilotons [Min <n>] [Max <n>]` | explosions | its yield |

The game's `Explodopedia.txt` writes the game's own placement out as rules (the units by class, the weapons by what
they are used against, the radars by what they detect, the research by field, the explosions in one), so it can be
edited in place; a page none of them matches still goes where the game puts it, unless its tab has `Auto No`.

Some values have a purpose in the game but look odd in an encyclopedia; the game's file hides two:

```
HideProperty Speed Of Weapons Where Name "Cyber Warfare"      // the cyber attacks are timed by a speed
HideModifier "Collateral_Damage_Modifier" Of Weapons          // x800000 damage against cities: collateral damage
```

The order of the categories in a tab is the game's (the unit classes', the fields' order), with a new category
after the one in its `After` (else last) and a moved one after the one in its `After`: where a line stands in the file
does not change it. A line the file does not understand stops reading it, with a warning naming the line (in
`Fatal.txt` and on the screen).

A category of the game that is wrong is fixed by emptying it (rules putting its pages elsewhere: an empty category
is left out), renaming it (`<key>_NAME` in `explodopedia.lng`), moving it (`After`) or, for a whole tab, `Auto No`
and categories of its own. The game's file sorts the radars this way:

```
NewCategory "CATEGORY_RadarOptics" Tab "Radars" After "CATEGORY_RadarSurface"
NewCategory "CATEGORY_RadarSatellite" Tab "Radars" After "CATEGORY_RadarOptics"
Put Radars Where ShowType SPACE_RANGES In "CATEGORY_RadarSpace"
Put Radars Where ShowType OPTICAL_RANGES In "CATEGORY_RadarOptics"
Put Radars Where ShowType SATELLITE_RANGES In "CATEGORY_RadarSatellite"
Put Radars Where DetectsNothing And ID "Satellite Relay*" In "CATEGORY_RadarSpace"
Exclude Radars Where DetectsNothing And ID "Resupply*"
```

A tab of categories of one's own, e.g. the explosions by yield:

```
Tab "Explosions" Auto No
NewCategory "CATEGORY_SmallYield" Tab "Explosions"
NewCategory "CATEGORY_BigYield" Tab "Explosions"
Put Explosions Where Kilotons Max 999 In "CATEGORY_SmallYield"
Put Explosions Where Kilotons Min 1000 In "CATEGORY_BigYield"
```

A mod's new weapon or sensor goes where it belongs with a `Put` in the mod's `Explodopedia.txt`
(`Put "My_Railgun" In "CATEGORY_Naval"`).

`Hide` leaves a tab or a category out, with all its pages: no other page links to them or shows their icons
(`Tab "Explosions" Hide`, `Category "CATEGORY_AntiSat" Hide`). `Hide No` brings one back, e.g. in a mod.

## 4. General information articles

The general tab starts with **Gameplay hints**: every hint of the language's `loading.lng`, numbered, in
the order of the file (a mod's hints added with `USE PREVIOUS` in its `loading.lng` appear there too). The
article chapters follow it.

| Key | Meaning |
|---|---|
| `GENERAL_<c>_TITLE` | chapter c = 1, 2, 3… in this order; the first missing number ends the chapters |
| `GENERAL_<c>_DESC` | the chapter's overview page |
| `GENERAL_<c>_<a>_TITLE` | article a = 1, 2, 3… of the chapter, in this order; the first missing number ends them |
| `GENERAL_<c>_<a>_FILE` | the article's text in a file of its own: `Lang/<language>/<file>`, the English one when the language has none. For long articles |
| `GENERAL_<c>_<a>_TEXT` | or the text in the key itself; more paragraphs as `_TEXT_2`, `_TEXT_3`… (a key holds up to 64 KB) |
| `GENERAL_<c>_<a>_IMAGE` | a picture beside the text, a file of the game's data, e.g. `"Images/VM/logo.png"` |

```
"GENERAL_1_TITLE" LANG "Lens On: Nuclear Weapons"
"GENERAL_1_DESC" LANG "How nuclear weapons shaped the second half of the twentieth century."
"GENERAL_1_1_TITLE" LANG "ICBMs and the Space Race"
"GENERAL_1_1_FILE" LANG "Explodopedia/General_1_1.txt"
"GENERAL_1_2_TITLE" LANG "A short one"
"GENERAL_1_2_TEXT" LANG "The text of the article, in the key itself."
```

An article's file is plain UTF-8 text (with or without a byte order mark):

* paragraphs are apart by an empty line;
* a line starting with `## ` starts a part of the article (a large heading);
* a line starting with `### ` is a heading inside a part.

A text that starts with a tag is HTML instead ([§5](#5-articles-in-html)).

## 5. Articles in HTML

An article's text (its file or its `_TEXT` keys) that starts with a tag, such as `<p>` or `<h2>`, is read
as basic HTML. Of styles, only bold and italic are used (`font-weight`, `font-style` in a `style` attribute or in
the class rules of a `<style>` block, as Google Docs writes them); everything else of HTML is ignored, with its
text kept: there are no colours, fonts, tables or scripts, and the text of `<head>`, `<title>`, `<style>` and
`<script>` is not shown. A whole page (`<!DOCTYPE html><html><head>…</head><body>…`) is read as well.

| Tags | Meaning |
|---|---|
| `<p>`, `<div>` | a paragraph |
| `<h1>`, `<h2>` | a part of the article (a large heading) |
| `<h3>` … `<h6>` | a heading inside a part |
| `<br>` | a new line |
| `<hr>` | a line across the column |
| `<b>`, `<strong>` | bold |
| `<i>`, `<em>` | italic (bold and italic together: bold) |
| `<ul>`, `<ol>`, `<li>` | lists, with bullets or numbers; lists inside lists are indented |
| `<a href="…">` | a link to another page of the Explodopedia |
| `<img src="…" width="…" align="…" alt="…">` | a picture |
| `<figure>`, `<figcaption>` | a picture with its caption under it |
| `<!-- … -->` | a comment |

Entities: `&amp;` `&lt;` `&gt;` `&quot;` `&nbsp;` `&mdash;` `&ndash;` `&hellip;` `&laquo;` `&raquo;`, the
quotes, `&deg;` `&times;` `&minus;` and the like, and numbered ones (`&#8212;`, `&#x2014;`).

Line breaks and spaces in the file do not matter: the text wraps to the column, between words, and between
the characters of Chinese text.

**Links**: `href` is the ID of a page or its name, case aside:

* a unit's ID or its technology's ID: `<a href="Fighter">`, `<a href="U_Fighter">`;
* a weapon's or radar's ID or its technology's ID: `<a href="M_ICBM_10M_Heavy">`;
* a research's ID; an explosion's ID (the page of its yield);
* another article: `GENERAL_<c>_<a>`, e.g. `<a href="GENERAL_1_3">`;
* or the page's name as shown in the list: `<a href="10 Megaton ICBM">`.

A link whose page does not exist is plain text. Back (the button, the mouse's back button, Backspace)
returns from a followed link.

**Pictures**: `src` is looked for in this order:

1. as written, from the game's folder (like the other pictures of the data: `Units/Images/…`);
2. beside the article's file;
3. in `Lang/<language>/Explodopedia/`, then `Lang/Eng/Explodopedia/`.

`width` is in percent of the column (`width="40%"`) or in pixels at 1920×1080 (`width="300"`, scaled with the
screen); without it, the picture's own size. A picture never gets wider than the column.
`align="left"` or `align="right"` puts it on that side, at most 60% of the column wide, with the text going
on beside it; without `align` it stands on its own line, centred, below any pictures on the sides. `alt` is
shown as a tooltip over the picture. A picture that is not found is left out.

```html
<h2>The Space Race</h2>
<p>In October 1957 the <b>Soviet Union</b> launched <i>Sputnik</i>, the first satellite.
If a rocket could put a satellite into orbit, it could also deliver a warhead: see the
<a href="M_ICBM_10M_Heavy">10 Megaton ICBM</a>.</p>
<img src="sputnik.png" width="35%" align="right" alt="Sputnik 1">
<ul>
  <li>4 October 1957: Sputnik 1</li>
  <li>3 November 1957: Sputnik 2, with the dog Laika</li>
</ul>
<figure>
  <img src="launch.jpg" width="80%">
  <figcaption>A launch of an R-7 rocket</figcaption>
</figure>
```

### Writing an article in Google Docs

An article can be written in Google Docs and used as it is downloaded:

1. Write it with the paragraph styles of Docs: **Title** and **Heading 1**/**Heading 2** become large headings,
   **Subtitle** and **Heading 3**–**6** smaller ones (text merely typed in capitals stays text). Bold, italic,
   bulleted and numbered lists (also nested ones) come through.
2. Links to other pages of the Explodopedia: Docs accepts only web addresses, so write the page's ID as one:
   link the text to `http://M_ICBM_10M_Heavy` or `http://GENERAL_1_3`. The game drops the `http://` and Docs'
   own redirect (`https://www.google.com/url?q=…`). A link to a real website is plain text in the game.
3. Pictures: insert them in line with the text (Docs' **In line**); each stands on its own line, centred, as
   wide a share of the column as of the Docs page (half the page: half the column). `alt` text (Docs: Image
   options → Alt text) is the tooltip.
4. **File → Download → Web page (.html, zipped)**. Unzip it into `Lang/<language>/Explodopedia/`: the `.html`
   (rename it, e.g. `General_1_11.html`) and its `images/` folder (its `src` are `images/image1.png`…, found
   beside the file). With several articles in one folder, give each its own pictures folder and change the
   `src` in its file accordingly, or the `images/` of one replaces another's.
5. Register it with `_TITLE` and `_FILE` keys ([§4](#4-general-information-articles)).

Colours, fonts, sizes and tables are not carried over (a table's text stays). Resolve the document's comments
before downloading: they are written into the file. Footnotes come out as plain text at the end. A picture
placed with text wrapping may not stand where it did in Docs: place pictures **In line**.

## 6. Step by step: adding an HTML article

This example adds a chapter "Cold War Notes" with one article, "Sputnik", with a picture and a link, as a
mod. To change the base game instead, put the same files straight into the game's `Lang/Eng/` folder and add
the keys to the game's `Lang/Eng/explodopedia.lng` (then without the `USE PREVIOUS` line of step 5).

**1. Make the mod.** Create the folder `Documents/My Games/ICBM-Escalation/MODS/ColdWarNotes/` with an
`info.txt` ([12 §2](12-Config-Files.md#2-mods-infotxt)):

```
ICBM MOD "Cold War Notes"
Version "1.0"
Description "Articles about the Cold War for the Explodopedia"
```

Everything below goes into this folder; its paths mirror the game folder.

**2. Pick the numbers.** Open the game's `Lang/Eng/explodopedia.lng` and find the last chapter:
the highest `GENERAL_<c>_TITLE`. The game has chapter 1, so the new chapter is **2** and its first article
**1**: the keys will be `GENERAL_2_TITLE`, `GENERAL_2_1_TITLE`... (To add an article to an existing chapter
instead, take that chapter's next free article number, e.g. `GENERAL_1_11_…` after the game's ten.) Numbers
must follow each other without gaps.

**3. Write the article.** Create `Lang/Eng/Explodopedia/Sputnik.html` in the mod, saved as UTF-8. Its very
first character must be `<`, or the file is read as plain text:

```html
<h2>The first satellite</h2>
<p>On <b>4 October 1957</b> the Soviet Union launched <i>Sputnik 1</i>, a polished sphere 58 cm
across that did nothing but beep. It circled the Earth every 96 minutes.</p>
<img src="sputnik.png" width="35%" align="right" alt="Sputnik 1">
<p>The rocket that lifted it, the R-7, had been built to carry a nuclear warhead across the ocean.
If it could reach orbit, it could reach any city: the beginning of the age of the
<a href="M_ICBM_10M_Heavy">intercontinental ballistic missile</a>.</p>
<h3>What followed</h3>
<ol>
  <li>3 November 1957: Sputnik 2, with the dog Laika on board.</li>
  <li>31 January 1958: Explorer 1, the first American satellite.</li>
  <li>29 July 1958: NASA is founded.</li>
</ol>
<p>Read on: <a href="GENERAL_1_1">ICBMs and the Space Race</a>.</p>
```

* `<a href="M_ICBM_10M_Heavy">` opens the page of the weapon with that ID; `href` can also be a unit's,
  radar's, research's or explosion's ID, another article's `GENERAL_<c>_<a>`, or a page's name as shown in
  the list ([§5](#5-articles-in-html)).
* The picture floats on the right with the text beside it; `width="35%"` is of the text column.

**4. Add the picture.** Put `sputnik.png` (PNG or JPG) next to the article:
`Lang/Eng/Explodopedia/sputnik.png` in the mod. `src` is found beside the article's file, so the article and
its pictures stay together.

**5. Register the article.** Create `Lang/Eng/explodopedia.lng` in the mod. Its first line keeps the game's
texts, and the keys after it add the chapter:

```
USE PREVIOUS "Lang/Eng/explodopedia.lng"

"GENERAL_2_TITLE" LANG "Cold War Notes"
"GENERAL_2_DESC" LANG "Short articles about the events behind the game."
"GENERAL_2_1_TITLE" LANG "Sputnik"
"GENERAL_2_1_FILE" LANG "Explodopedia/Sputnik.html"
```

`_FILE` is relative to `Lang/<language>/`. Without `USE PREVIOUS`, the mod's file would replace the game's
and the game's own articles and category descriptions would be gone.

The mod now holds:

```
MODS/ColdWarNotes/
  info.txt
  Lang/Eng/explodopedia.lng
  Lang/Eng/Explodopedia/Sputnik.html
  Lang/Eng/Explodopedia/sputnik.png
```

**6. Check it in the game.** Enable the mod in the mod list, open the Explodopedia from the main menu and go
to the general tab (the globe): after Gameplay hints and the game's chapter there is an icon for "Cold War
Notes"; its overview lists "Sputnik". Check that:

* the headings, bold and italic words and the numbered list look right;
* the picture is on the right (missing: the `src` name or the file's place, [§8](#8-pitfalls));
* the links are green and open their pages, and Back (the button, the mouse's back button or Backspace)
  returns to the article. A link shown in white found no page: check its `href`.

The Explodopedia reads its texts and articles each time it opens: after editing the `.lng` or the `.html`
file, close it and open it again. A picture stays loaded once shown: to see a changed picture, restart the
game (or give the new version another file name).

**7. Translate it (optional).** For Russian, add `Lang/Rus/Explodopedia/Sputnik.html` (the translated
article) and `Lang/Rus/explodopedia.lng` with `USE PREVIOUS "Lang/Rus/explodopedia.lng"` and the translated
`GENERAL_2_TITLE`, `GENERAL_2_DESC` and `GENERAL_2_1_TITLE`. The `_FILE` key can stay in English only: the
game looks for the file in the language's folder first. The picture need not be copied: it is found in
`Lang/Eng/Explodopedia/` too. Anything the language lacks is shown in English.

## 7. Mods and translations

A mod adds its texts with its own `Lang/Eng/explodopedia.lng` that starts with a `USE PREVIOUS` of the
game's file ([00 §3](00-Basics.md#3-mods-and-file-overriding)), then adds or replaces keys:

```
USE PREVIOUS "Lang/Eng/explodopedia.lng"

"CATEGORY_UC_Orbital" LANG "Orbital platforms of the mod: ..."
"GENERAL_2_TITLE" LANG "My mod's history"
"GENERAL_2_1_TITLE" LANG "How it began"
"GENERAL_2_1_FILE" LANG "Explodopedia/MyMod_2_1.html"
```

A later key replaces an earlier one with the same name, so a mod can also rewrite the game's texts. Adding
the next free chapter number (`GENERAL_2_…` after the game's chapter 1) adds a chapter; keep the numbers
without gaps, since the first missing number ends the list.

A translation is `Lang/<language>/explodopedia.lng` with the same keys; article files go to
`Lang/<language>/…` under the same names. Keys and files the language lacks show in English.

## 8. Pitfalls

* **No page**: the object's technology has no name in the language files, the missile is `Hidden`, the
  radar has `DoNotShow`, or the object has `DoNotShowInEncyclopedia`.
* **A gap in the numbers** ends the chapters or articles: `GENERAL_1_3` is never read when `GENERAL_1_2_TITLE`
  is missing.
* **An HTML article shown as plain text with its tags**: the text does not start with a tag (look for text
  or a stray character before the first `<`).
* **Chinese, Japanese or Korean in an article** shows only in a language whose fonts have those characters
  (`codepage.table`, [12 §5](12-Config-Files.md#5-language-files)); the Latin fonts leave them blank. A
  language's fonts may have no bold or italic version of them.
* **A picture is missing**: the `src` path is not found in any of the places of [§5](#5-articles-in-html);
  paths are relative, with `/`.
* **A long text in a key** is cut at 64 KB: use `_TEXT_2`, `_TEXT_3`… or a file.
