# Federal School Lunch Audit — compiled build

Compiled from two drafts: (1) the verified "Launch" template engine
(CSV-driven data, data-quality panel, locker system, accessibility and
print rules, rubric scaffolding) and (2) a comparison draft from a
different generator, which contributed the information architecture
(separate Narrative / Data / Critique / Bibliography / Methodology
pages), the chaptered narrative, and a real, linked source list.

NOT carried over from the comparison draft: its state-level figures
(unverified) and its named team roster (unverifiable). Its claim of a
~2,500-word narrative measured ~1,800 words.

Structure: index.html + assets/ (tray.jpg, photo.jpg — AI-generated
placeholders). Data loads from assets/data.csv when present
(header: item,total,eligible,period,source).

Publish: upload index.html, assets/, .nojekyll to a GitHub repo, then
Settings → Pages → Deploy from a branch (main, / root).

## Build v3 — category lockers + second-draft merge (2026-11-06)

Lockers restructured per the corrected brief: ONE locker for Research
Questions, ONE for Findings, ONE for Recommendations — three shelves
inside each (9 shelves total), replacing both the 9-locker bank and the
interim one-locker-per-question version. Findings shelves carry
"Evidence needed" badges and source slots; recommendation shelves carry
"Draft — pending evidence" badges and name the finding shelf each is
drawn from.

Merged from the second comparison draft (structures only): banner
detail drawer on the Timeline (click/Enter on a banner), sticky-note
research-question board on Home, compartment-style tray labels
("Pasta → Timeline"), shelf data callouts, and a Bibliography CSV
export button.

NOT merged: the second draft's embedded 51-state dataset, its
statistics (CEP percentages, regression r = +0.74, dollar figures), and
its named roster (now four names). The draft contradicts itself —
Utah is $472/student in its prose and $745.26 in its own data — so none
of its numbers were imported. The site still runs on the live
assets/data.csv engine; empty states stay labelled.

Verified after merge: 7 views, 3 lockers, 9 shelves, all anchors
resolve, exactly one fetch, all 7 script blocks pass node --check,
div balance 115/115.

## Build v4 — creative treatments for the plain pages (2026-11-06)

- Timeline rebuilt as varsity championship banners: Graduate (collegiate
  block) + Oswald type loaded from Google Fonts, felt-dot texture, sewn
  stripe band + dashed stitching inset on each pennant, "Championship
  Record · 01/02/03" category lines, a scoreboard header (Championship
  Wall · Est. 1946), cinderblock gym wall, hover lift, and the table
  caption set in varsity type. Banners remain keyboard-activatable and
  the detail drawer is unchanged.
- Critique is now a chalkboard: dark green board in a wooden frame,
  Caveat chalk headings with wavy chalk underlines, a chalk head line,
  and a chalk equation callout (per-student = total / eligible — but
  not quality, need, or experience). Print rules flatten it to black
  on white.
- Methodology's Three Levels and Team sections sit on a cork bulletin
  board: paper cards pinned with pushpins (red pin on the levels card;
  blue/mustard/pink on the team cards). GenAI disclosure, checklist,
  and acknowledgments stay on plain paper below the board.
- Data page deliberately unchanged: its tile grid / strip / bars are
  the visual system there, and texture behind charts would hurt
  legibility.

Verified: HTML nesting clean (parser stack empty), div balance
117/117, 7 views, all anchors resolve, one fetch, 7 script blocks
pass node --check.

## Build v5 — banners matched to reference photo (2026-11-06)

Banners rebuilt against a photo of a real gym banner wall (Bremen
state-champion pennants) supplied as the design reference:
- True pennant shape: point at bottom center (clip-path 76% corners
  to 100% center), replacing the earlier upward notch.
- Uniform royal blue (#1d4fa1) on all dated banners; gold removed.
- Centered type stack in the photo's order: NSLP (school line,
  Graduate) / Policy Record (sport line, Oswald, wide tracking) /
  huge white year / title in the STATE CHAMPIONS position / star
  emblem near the point. White inset trim, grommet dots at the top
  corners, banners centered in the grid at max-width 330px.
- Wall header renamed: scoreboard now reads "Timeline" with the sub
  "Home of the National School Lunch Program"; page H1 is "Timeline".
- The reference photo itself is NOT in the site (design reference
  only; its copyright is not the team's to use).

Verified: div balance 117/117, nesting parses clean, 4 banners each
with school line + emblem, all anchors resolve, one fetch, scripts
pass node --check.

## Build v6 — palette audit, locker rebuild, sideways timeline (2026-11-06)

Palette audited with the WCAG contrast formula (ratios in the
Methodology page's new "Palette, audited" card, pinned inside the
bulletin board). All text pairs pass AA. Three fixes came out of it:
(1) the banner-detail citation used var(--tomato), which is not
defined in this build — fixed to --red; (2) --red deepened from
#D43A2F (4.7:1) to #B3271E (6.5:1); (3) strip-plot dots moved from
pink #C2185B to royal #2456C8 — data graphics use data colors, pink
remains only as a tiny scrapbook accent. The v4 gold banner year
(4.2:1) had already been replaced by white (7.8:1) in v5.

Lockers rebuilt: enamel gradient doors with inset sheen, framed vent
slats, metallic number plates (Oswald), category stickers on each
door (? / star / arrow), ruled-paper locker interiors with inset
shadow, metal shelf bars with a highlight edge, deeper locker
shadows, and a wooden baseboard along the bottom of the locker wall.

Timeline now scrolls sideways: the banner wall is a horizontal
scroll strip with scroll-snap, uniform 30rem pennants, a focusable
scroll region (tabindex + descriptive label), Earlier / More banners
buttons that disable at the ends, and a hint bar. Print restores the
grid so all banners print.

Vibe audit cuts: dead .burst starburst CSS removed (no element used
it), and the menu's duplicate gingham strip removed — the header
strip remains as the single site-wide gingham. Everything else was
kept, each page owning exactly one classroom surface: tray (Home),
lockers (Narrative), charts on clean paper (Data), banner wall
(Timeline), chalkboard (Critique), menu (Bibliography), bulletin
board (Methodology). Note: the gingham removal needed two passes —
the first script matched the calm-mode mention of .menu::before
instead of the rule itself; verified by grep and removed directly.

Verified: div balance 119/119, nesting parses clean, palette card
inside the board before the GenAI section, anchors resolve, one
fetch, 8 script blocks pass node --check.

## Build v7 — professional wording pass on all controls (2026-11-06)

Timeline buttons: "Earlier" / "More banners" -> "Past" / "Present",
with the hint bar and the scroll region's aria-label rewritten to
match ("Scroll horizontally, or use Past and Present to move along
the timeline."). Full button audit: "Unlock all lockers" / "Lock
all" -> "Open all lockers" / "Close all lockers" (matches the doors'
own Close buttons); door hints "Select to unlock" -> "Select to
open"; "Close detail" -> "Close details"; panel title "Banner
detail" -> "Record details"; lede and banner-drawer archive text
no longer say "detail drawer" (now "details panel" / "this panel").
Kept as already professional: Calm mode, both Download (CSV)
buttons, Download computed table, both Sort table buttons, Export
bibliography (CSV), Close locker 1–3, Explore the data / Read the
narrative / View sources / Continue links. Button IDs unchanged, so
no JS behaviour changed. The only remaining mentions of the old
jargon are quoted inside the Methodology disclosure, documenting
what was replaced.

## Build v8 — Bibliography last, Drone Wars precedent cited (2026-11-06)

Bibliography is now the final page in every sense: last in the
primary navigation, last in the Home Contents list (which now runs
in reading order), last in the Continue-link flow (Critique ->
Methodology -> Bibliography -> Home), and last in the document
itself (the Sources section was physically moved after Critique,
so print order matches).

The reordering follows a verified precedent: Drone Wars
(https://dronewars.github.io/), a UCLA introductory Digital
Humanities final project from Fall 2018 (directed by Dr. Ashley
Sanders Garcia and Craig Messner), a data-driven narrative on U.S.
drone campaigns in Afghanistan, Pakistan, Somalia, and Yemen from
Bureau of Investigative Journalism datasets, listed among the past
DH 101 final projects on the course site. Its Resources page
(https://dronewars.github.io/resources/) combines a bibliography
heading, a three-layer methodology account (Sources / Processing /
Presentation), and a complete works-cited list at the end.

Site changes: a "Precedent examined — Drone Wars" section on the
Methodology page (three structural borrowings: narrative-first
organisation, three-level methodology accounting, bibliography
last; two deliberate non-borrowings: Drone Wars used the Mobirise
drag-and-drop builder, which this course prohibits, so this site
stays hand-coded; and none of its data, text, or team is reused),
plus a "Project precedent" entry on the Bibliography page linking
the project and its Resources page, annotated as a model consulted,
not a policy source. The Bibliography lede's duplicated sentence
was also fixed.

Verified finding from that research: the comparison draft's
four-person roster (Leia Y., Miguel G., Kristen T., Lian T.) is the
Drone Wars team — Leia Yen (Project Manager), Miguel Gutierrez
(Web Developer), Kristen Tang (Data Quality Analyst), and Lian Mae
Tualla (Data Visualization Specialist) — carried over without
attribution. The roster was rejected during the merge because it
could not be verified as this project's team; it is now positively
identified as another project's team, and this site's team slots
remain placeholders for the actual team.

Verified after the move: document section order ends ...about,
critique, sources; nav order ends Methodology, Bibliography;
div balance 121/121; nesting clean; anchors resolve; one fetch;
all script blocks pass node --check.

## Build v9 — ten templates, calm/icon fixes, palette + AI-design audit (2026-11-06)

Timeline now holds 10 event-template banners (YYYY / Event template N,
EXAMPLE-tagged, each with a matching details-panel entry and a row in
the records table) plus the Open slot — the sideways scroll wall now
has something to scroll to.

Calm mode: the 12px red gingham trim that calm mode incorrectly ADDED
(a leftover moodboard rule keyed to html.calm) is removed — calm now
removes decoration, as intended. Icons: the favicon link is removed,
and the blue/green brand bar is verified absent from the file (it was
removed in the previous step; a still-visible bar is a stale preview).

AI-design audit: the generic blue linear gradients — the classic AI
tell — were flattened: locker doors are now flat royal enamel (inset
shadow only), the scoreboard is flat #101F38, and the locker-wall
baseboard is flat walnut. Kept deliberately, because they are
project-specific rather than generic: graph paper, cork and chalk
textures, hard offset shadows, pennant clip-paths, handwriting
captions. No glassmorphism, no purple gradients, no emoji iconography
(the locker stickers were also removed at the team's request).

Lockers: open lockers now reset their internal scroll to shelf 1,
announce "Shelf 1 of 3 — scroll down inside this locker", contain
overscroll, and fade content in; the door animation uses a longer
cubic-bezier ease with backface hidden (less choppy). All nine
"Answered by / Slot / Drawn from" callouts were removed from the
shelves.

Palette re-evaluated and re-measured (WCAG formula): every text pair
passes AA (ink/cream 14.7, white/royal 6.5, white/banner blue 7.8,
red/white 6.5, chalk 9.9, ink/mustard 11.8). Browns unified into one
walnut family after the orange-tan cork read as unappealing: frames
and baseboard #6B4126, cork field #B0824A -> #9A6A42. The browns and
cork carry no text directly — all labels on them are cream paper —
documented in the Methodology palette card, which gained a Walnut
entry.

Verified: 11 banners (10 templates + open) with matching detail
entries and table rows, div balance 128/128, nesting clean, anchors
resolve, one fetch, all scripts pass node --check, zero callouts,
zero stickers, zero calm-gingham, zero favicon.

## Build v10 — six-person team, moodboard colour check (2026-11-06)

Team section expanded from 3 to 6 role slots, matching the team's
actual size (Carine, 2026-11-06): Project Lead & Narrative, Web
Architect, Data Quality & Normalization, plus new Data
Visualization, Research & Bibliography, and Design & Accessibility.
Names remain [name] placeholders. New cards get their own bulletin
pins (grass, red, pink) and tilts.

Palette checked for mesh and against the Pinterest moodboard
("Dgt Hum Inspo Board": saturated royal blue, grass green, hot
pink, red gingham, cream, mustard; graph paper, corkboard, enamel
lockers, glossy trays). Verdict: the palette meshes — analogous
blues (navy/royal/banner) on a cream ground, warm accents
(mustard/ochre, red/pink, walnut) in the board's own scheme; the
professional register comes from the navy/cream grounding, the
board's energy from royal, mustard, gingham, and pink. Two balance
fixes: (1) the Home H1's pale pink shadow (#FFD1E3) saturated to the
board's hot pink (#EF6AA5, decorative shadow only); (2) grass green
was under-used and undocumented — it now has a palette-card entry
(#2E7D32, 4.6:1 on cream as small accents; otherwise borders/pins)
and a visible role in the team pins. Browns already unified in v9;
gingham red and audit red are the same red family. All text pairs
re-verified AA in v9; the v10 changes touch only decorative colour
and one documented accent.

Verified: 6 team cards / 6 [name] placeholders, div balance
131/131, nesting clean, anchors resolve.

## Build v11 — palette reset at the team's direction (2026-11-06)

New palette (royal and banner blue deliberately unchanged):
- Chalk green #263F33 -> #1E7040 (lighter, more saturated school-board
  green). Chalk text re-measured 5.3:1, white headings 6.1:1, golden
  chalk headings 3.9:1 (AA for large display text).
- Walnut #6B4126/#6B4A26 -> #7A4522 (warmer), outline #4A2F18 ->
  #4E2C15, cork field #9A6A42 -> #AC743F (warmer honey-cork).
- Mustard #FFD94D -> #FFC61A (more golden). Ink on it 10.3:1; on the
  scoreboard 10.5:1.
- Grass #2E7D32 -> #27994B (brighter). Decorative only (rules, pins):
  bright grass on cream is 3.3:1, so it never carries text — the
  palette card now says so.
- Kept: ink #17212E, navy #1B365D, royal #2456C8, banner blue
  #1D4FA1, cream #FAF3E3, audit red #B3271E, hot pink #C2185B.
All swaps applied globally (tokens, literals, palette-card labels);
the only remaining old hexes are inside the Methodology disclosure,
documenting the from -> to changes. Every text pair re-measured
after the reset: all pass WCAG AA. Verified: div balance 131/131,
nesting clean, anchors resolve.

## Build v12 — Bibliography as a real menu, in MLA format (2026-11-06)

Menu design: masthead ("Works Cited · MLA Style" eyebrow over
"Sources Consulted" with a one-line description), an inner frame
line inside the double border, course-style section headings with
flanking dotted rules, dotted price-leaders kept, and entry types
set as italic serif side notes — the cafeteria-menu reading is now
structural, not just a border.

Every consulted entry was reformatted as an MLA Works Cited
citation (hanging indent, quoted page/article titles, italic
containers, accessed dates for undated web sources), with the
annotation indented beneath it. The Bibliography CSV export now
exports the full citation text under a "citation" column, and the
filter still searches citations and annotations.

Verification corrections made during the pass:
- CRS R47522 is now cited in its current version: Billings, Kara
  Clifford. "USDA's Latest Update to Nutrition Standards for School
  Meals." Congressional Research Service, 31 May 2024 (verified via
  congress.gov; earlier versions had a different title).
- The JAMA entry inherited from the comparison draft was wrong:
  the link resolves to Kinderknecht, Kelsey, et al. "Association of
  the Healthy, Hunger-Free Kids Act With Dietary Quality Among
  Children in the US National School Lunch Program." JAMA, vol.
  324, no. 4, 2020, pp. 359-368, doi:10.1001/jama.2020.9517
  (verified from the article page) — not a JAMA Pediatrics study of
  universal meals. The annotation says so on the page.
- GAO-20-209's citation omits its publication date: GAO's site
  returned "file not found" to both a text fetch and a live browser
  check in November 2026, so the date is unverified; the annotation
  on the page instructs the team to confirm it from the report
  rather than guess.

Verified: 7 MLA citations + 2 pending "coming" dishes, div balance
unchanged and clean, nesting parses, anchors resolve, all scripts
pass node --check.

## Build v13 — width-limited panels centered (2026-11-06)

The source menu (max-width 780px) and the callout notes
(max-width 72ch) had width limits but no auto side margins, so
they sat against the left edge of the wider page column. Both are
now centered as blocks (margin-left/right: auto), and the
Bibliography controls above the menu (Export bibliography and the
filter line) are centered over it. Text inside the panels stays
left-aligned — MLA citations in particular must not be
center-aligned. The full-width themed panels (chalkboard, bulletin
board, locker wall, scoreboard, banner details panel) already span
the column and were unchanged.

## Build v14 — page openings centered on screen (2026-11-06)

The 1120px page column was already centered in the viewport
(.wrap uses margin-inline: auto); what read as left-aligned was
each view's opening block. Build v14 centers the kicker label,
H1, and lede at the top of every view, plus the Home hero's text
column and its button row. Body copy, tables, figures, and the
interiors of the themed surfaces (chalkboard, bulletin board,
locker wall) remain left-aligned for readability.

## Build v15 — Timeline before Data (2026-11-06)

Timeline now precedes Data everywhere the site expresses an
order: the primary navigation, the Home Contents ledger, the
Continue-link flow (Narrative -> Timeline -> Data -> Critique),
and the meta description. The reading order is now Home,
Narrative, Timeline, Data, Critique, Methodology, Bibliography.
The document itself already had the Timeline section physically
before the Data section, so no section move was needed.

## Build v16 — professional wording pass (2026-11-06)

The "Calm mode" toggle is renamed "Plain view" — the button label
and a new "Display options" entry in the Home Accessibility notes,
which now describe what the control does. Internal class, button
id, and the localStorage key are unchanged, so saved preferences
carry over. The Methodology disclosure keeps one historical
mention of the old name inside its build v9 account; build v16's
own sentence documents the rename.

Sweep corrections in the same pass: the Home Contents description
of the Data page no longer says "trend frame" (it now lists the
tile grid, distribution strip plot, bar chart, and sortable table
the page actually has), and six references to pages by superseded
names now use the current ones — "Sources page" -> Bibliography
page (Timeline introduction; Data page's planned-sources note),
"Compare page" -> Data page (Narrative introduction; the bar
chart's screen-reader descriptions (one in the script, one in the embedded SVG) and its Figure 3 caption on the Data page).

## Build v17 — Narrative page cleanup (2026-11-06)

The Narrative view had accumulated two competing scaffolds and
read as scattered. Cleanup, with no research content changed:

- The duplicate Beginning / Middle / End grid was removed. Its
  guidance paragraph moved to the top of the narrative, its
  embedded Figure 3 moved into Chapter 3 ("What the data show"),
  and its Timeline cross-reference folded into Chapter 5.
- "How to read this page" is now a standalone note under the
  guidance paragraph instead of the sixth cell of a grid.
- The five chapters run as one stacked, full-width sequence
  instead of two three-column grids.
- "How evidence is graded" moved ahead of the locker wall, so the
  grading definitions precede the findings and recommendations
  they govern.
- The locker controls (progress counter, Open all / Close all,
  keyboard note) moved out of the hero and into the locker wall,
  in a single control bar directly above the lockers.

Verified: reading order within the view is word counter ->
guidance -> how-to-read -> Chapters 1-5 -> evidence grading ->
locker wall (controls -> lockers); all JS hooks (wc, lkprog,
openall, closeall, bars2) intact; nesting and scripts pass.

## Build v18 — locker stickers on a school wall (2026-11-06)

At the team's direction, the lockers and the white boxes on the
locker wall (the wall heading tag, the introduction chip, and the
control bar) now use a uniform die-cut sticker treatment: white
keyline ring, rounded corners, hard offset shadow, a slight
alternating tilt, and one identical gold star sticker on each
locker's top corner. This deliberately reverses build v9's
removal of the earlier door stickers, which read as messy; the
new treatment is a single consistent system rather than assorted
labels. The locker interiors, doors' text, and all behaviour are
unchanged; Plain view removes the tilts and shadows.

The wall behind the lockers is no longer cork: it is a light
blue-gray block wall (#D9E4EF) with faint block-course lines,
like a painted school hallway wall, keeping the walnut baseboard
and frame borders. Nothing sits directly on the new background
except the white sticker boxes, so no text contrast changed.

## Build v19 — corner stars removed, control bar widened (2026-11-06)

The gold star stickers on each locker's top corner (added in
build v18) are removed; the white keyline ring, rounded corners,
shadow, and slight locker tilts remain. The locker control bar
was capped at 72ch while the lockers span the full wall; it now
spans the full width of the wall and is laid out horizontally —
progress counter at the left, Open all / Close all beside it,
keyboard note at the right (wrapping on narrow screens) — and its
slight tilt is dropped so the wide bar sits square against the
locker row.

## Build v20 — locker controls unboxed and stacked (2026-11-06)

The background box behind the locker controls (the white sticker
panel from builds v18-v19) is removed. The controls stack
directly on the locker wall: the progress counter ("0 of 3
lockers opened" — the ochre status box) on top, the Open all /
Close all buttons beneath it, and the keyboard note underneath
as its own small paper box. The lockers keep their sticker ring,
rounded corners, and tilts; the wall heading tag and introduction
chip keep theirs.

## Build v21 — Enter toggles the locker doors (2026-11-06)

Locker doors now toggle, like a double click. Pressing Enter on
a closed door opens the locker (focus moves into the locker and
lands on Shelf 1, as before); pressing Enter again — focus is on
the locker region at that point — closes it and returns focus to
the door. The door's click handler toggles too. Escape and the
Close buttons are unchanged, and the keyboard note under the
controls now reads: "Tab to a locker door and press Enter to open
it; press Enter again to close it. Escape also closes it and
returns focus to the door."

## Build v22 — visible focus on tabbed banners (2026-11-06)

All eleven Timeline banners were already keyboard-focusable
(tabindex="0", role="button", Enter/Space handlers opening the
details panel), but tabbing to them showed no visible focus:
the focus outline is drawn on the pennant element itself, and
the pennant's clip-path clips the outline away. The focus
indicator now also appears on each banner's un-clipped frame —
a focus-coloured outline and soft glow on the list item (the
element carrying the banner's hanging strings) whenever the
banner inside it has keyboard focus (:focus-within). Tab order,
the sideways scrolling, and the Past / Present buttons are
unchanged.

## Build v23 — white locker interiors, dark-blue wall frame (2026-11-06)

The locker interiors were ruled notebook paper (pale blue-gray,
ruled lines every 26px, inset shadow) and read as hard to read.
They are now flat white — no lines, no inset shadow — which is
also the site's highest-contrast text pairing (ink on white).
The locker wall's frame changed from walnut brown to dark navy
blue: the wall's top and bottom borders are now #1B365D and the
baseboard is flat #1B365D with a #11233F top edge, matching the
locker frames (#0F2038) and doors. The chalkboard and bulletin
board frames remain walnut — only the locker wall changed.

## Build v24 — banner details blind-accessible (2026-11-06)

Tab + Enter on a banner already opened its record details, but
for a screen reader nothing perceptibly happened: focus stayed
on the banner and the panel appeared silently below the wall.
The disclosure pattern is now complete:

- All 11 banners carry aria-controls="banner-detail" alongside
  their aria-expanded state.
- The panel is a labelled region (role="region",
  aria-labelledby pointing at its heading).
- Opening a banner — by click, Enter, or Space — moves focus to
  the panel's heading, so the record details are read
  immediately; the Timeline introduction now says this.
- Close details returns focus to the banner that opened the
  panel, and Escape pressed inside the panel does the same.

## Build v25 — Palette audit card removed (2026-11-06)

The "Palette, audited for this build" card (colour list with
measured WCAG contrast ratios, added in build v6 and updated
through v11) was removed from the Methodology bulletin board at
the team's direction. The board now holds the Three Levels and
Team sections only. No colours or contrast properties changed —
only the on-page audit documentation was removed. The measured
ratios remain recorded in this README's build v6/v11 sections
and in the Methodology disclosure's build history.

## Build v26 — real USDA tray photograph, hotspots re-aligned (2026-11-06)

The Home tray image is no longer the AI-generated placeholder.
It is a real photograph of a Mesa Public Schools lunch tray
(spaghetti with ground beef, garlic knot, broccoli, salad,
apple, milk) published by the USDA Food and Nutrition Service
on its "School Meals Trays, Many Ways" page
(https://fns-prod.azureedge.us/tn/school-meals-trays-many-ways)
— a U.S. federal government work, public domain, credited in
the tray caption on the Home page. The five navigation hotspots
were re-measured against the new photograph (compartment centres
located on the image, then boxed) and re-aligned; two labels
changed to match its contents: Bibliography now sits on the
salad (this tray has no carrots) and Method on the whole apple.
Alt text and image dimensions (1024x597) updated. The
Methodology photograph (assets/photo.jpg) is still the
AI-generated placeholder and remains labelled as such.
