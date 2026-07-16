# Changelog

All notable changes to this project are documented here.

---

## v10 (Current)

- Fixed Most Pulled Cards merging shared Major Arcana names across Sailor Moon and Erotic Tarot — now keyed by `deck::cardname`
- Added duplicate card row button (⧉ Copy) for faster spread building
- Added `openModalByIndex` function — fixes Heaven & Hell cards not being clickable

---

## v9

- Added section headers within spreads for grouped multi-section layouts (e.g. FS Spread)
- Added FS Spread template with 6 named sections
- Added up/down reorder buttons (▲▼) on card rows and section headers
- Added collapsible sections in pull history
- Added sticky navigation bar
- Added back-to-top button
- Added jump-to nav within Sailor Moon, Erotic Tarot, and AGR pages
- Added deck profiles on each deck page with usage guidelines and system role
- Corrected Heaven & Hell card names against Obsidian index (Menadel, Vepar, Uvall, Lauviah, Louviah, Leuuviah)
- Fixed Heaven & Hell cards not opening modal on click

---

## v8

- Added orientation breakdown to Most Pulled Cards (upright vs reversed bar + percentages)
- Added Card History Search — find every spread a specific card appeared in with orientation summary
- Replaced Google Fonts with system font stacks — works fully offline

---

## v7

- Replaced Google Fonts import with system font stacks (Georgia, system-ui)
- All features from v6 preserved

---

## v6

- Added 12 new tags: Fun, Social, Travel, Fantasy, Erotic, Grief, Money, Health, Past, Future, Dream (19 total)
- Added pagination to pull history — 8 spreads per page with prev/next, page numbers, and ellipsis
- Page resets to 1 on filter, tag, sort, or search change

---

## v5

- Fixed card notes collision between Sailor Moon and Erotic Tarot Major Arcana — notes now keyed by `deck::cardname`

---

## v4

- Added Overall Synthesis field to spread log form
- Synthesis displays in pull history under each spread
- Synthesis restores correctly on edit; clears on clone

---

## v3

- Added AGR card meanings across all 9 Temples (meaning, shadow, embodiment question)
- Added Kimbition card meanings (spiritual/reflective interpretations for all 45 cards)
- Fixed card modal breaking on apostrophes in meanings — switched to index-based modal opening

---

## v2

- Added localStorage persistence for pull history and card notes
- Added export to JSON backup
- Added import from JSON backup
- Added clear all data option

---

## v1

- Initial build
- Full card reference for all 5 decks
- Pull tracker with deck, card, position, orientation, and card notes
- Spread templates
- Tags (8 initial)
- Most Pulled Cards stat
- Card lookup with search and deck filter
- Soft feminine aesthetic with blush, lavender, and rose gold palette
