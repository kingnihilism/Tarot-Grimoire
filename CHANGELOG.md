# Changelog

All notable changes to this project are documented here.

---
## v12 (Current)

### Added
- Added light and dark mode with persistent theme preference
- Added a floating theme toggle in the bottom-left corner
- Added Pull History pop-ups for viewing complete saved spread details
- Added four new spread tags:
  - 🔎 Check-In
  - 🧭 Decision
  - 🗓️ Forecast
  - 🕯️ Deity
- Added Sideways and Unclear card orientations alongside Upright and Reversed
- Added gold styling for the Other orientation category in Most Pulled Cards
- Added Erotic Tarot keyword chips based on each card's Core Erotic Function
- Added Erotic Tarot keyword matching to Card Lookup
- Added expanded source-reference meanings from the deck reference PDFs

### Improved
- Changed deck and suit navigation from page jumps to in-place content filtering
- Added All filters for returning to complete deck views
- Improved spacing between card meaning sections for easier reading
- Improved Pull History browsing by opening spreads in a dedicated modal
- Preserved Edit, Clone, and Delete controls separately from the Pull History pop-up
- Updated orientation statistics so Sideways and Unclear cards are counted as Other instead of Upright
- Improved light and dark mode styling across navigation, modals, forms, tags, badges, and spread panels
- Audited Heaven & Hell Oracle angel and demon pairings against the provided PDF
- Corrected Heaven & Hell light and shadow meanings to match the source material
- Removed citation-style trailing reference numbers from displayed source explanations
- Simplified card orientation options after testing by removing diagonal and custom rotation choices
---

## v11

### Added
- Added editable deck-specific upright and reversed meanings for Sailor Moon and Erotic Tarot Major Arcana
- Added separate localStorage persistence through `marcyDeckMeanings`
- Included deck-specific meanings in JSON export, import, and clear-data operations
- Expanded AGR and Kimbition Card Lookup search to match card keyword arrays
- Added visible matching keywords beneath relevant search results

### Improved
- Updated all card-list modal links to use `openModalByIndex`
- Standardized modal behavior across all five decks
- Improved Card Lookup discoverability for thematic searches such as water, healing, and shadow
---

## v10

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
