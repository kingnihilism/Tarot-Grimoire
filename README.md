# 🌿 Marcy's Deck Grimoire

A browser-based tarot, oracle, and Lenormand reference, spread logging, and pattern-tracking application built with **HTML, CSS, and vanilla JavaScript**.

The project supports a six-deck practice with different card structures, meanings, and roles while remaining fully offline. It includes searchable card references, customizable spread logging, deck-specific notes and meanings, statistics, filtering, JSON backups, and a documented GitHub Wiki.

## Live Project

- **Live application:** https://kingnihilism.github.io/Tarot-Grimoire/
- **Repository:** https://github.com/kingnihilism/Tarot-Grimoire
- **Wiki:** https://github.com/kingnihilism/Tarot-Grimoire/wiki
- **Current Version:** v14 — Romantic Lenormand Expansion

## Romantic Lenormand

Open **Romantic Lenormand** to browse 37 card profiles by name, number, keyword, or polarity. The deck has 36 numbered positions and two alternatives for #12. Select either Birds or Owls for a reading. The profiles paraphrase the Lo Scarabeo guidebook (Anna Oginsky, March 2024) and label supported timing separately from your personal notes.

Open **Lenormand Pull Tracker**, choose a quick template, then enter the cards you physically pulled in order. Lenormand is upright-only and has positive, negative, and neutral guidebook classifications. Available layouts are single card, three- and five-card lines, nine-card box, Grand Tableau (four rows of eight plus four), and custom. Use positions for positional readings or Overall Synthesis for a continuous sentence. The saved reading also retains individual card notes, reflections, tags, and category.

The combination encyclopedia counts contiguous sequences in their recorded order. Sequences inside mixed-deck readings stop at non-Lenormand cards. Add or edit personal combination interpretations and open the associated readings directly. The Lenormand tracker displays its eight most frequently pulled cards, polarity totals, category frequencies, and a collapsible combination encyclopedia. Its Card History Search and paginated Pull History provide editing, duplication, deletion, sorting, and tag filters. The regular Pull Tracker handles Tarot and Oracle. Mixed-deck readings remain accessible in both relevant views.

JSON backups include the new reading fields, combination interpretations, and theme. Earlier backups can still be restored. The application runs from the single HTML file without a network connection.

## Project Goals

Marcy's Deck Grimoire was created to solve several practical problems:

- Keep six tarot, oracle, and Lenormand decks in one searchable reference
- Preserve deck-specific meanings instead of treating shared card names as identical
- Log complex, multi-section spreads without relying on paper notes
- Track recurring cards, orientations, tags, and themes over time
- Store personal data locally without requiring an account, server, or internet connection
- Practice front-end development, data modeling, debugging, technical documentation, and version control

## Decks

| Deck | Type | Cards | Application Role |
|---|---:|---:|---|
| Sailor Moon Tarot | Tarot | 78 | Main narrative and traditional tarot structure |
| Erotic Tarot | Tarot | 78 | Intimacy, desire, and relationship dynamics |
| African Goddess Rising Oracle | Oracle | 44 | Goddess archetypes organized across 9 Temples |
| Kimbition Oracle | Oracle | 45 | Desire, fantasy, kink, and power archetypes |
| Heaven & Hell Oracle | Oracle | 72 | Angel and demon pairs representing alignment and distortion |
| Romantic Lenormand | Lenormand | 37 | Practical circumstances, interactions, and developments |

## Features

Both tracker views share a consistent responsive interface. Lenormand statistics and combinations appear below its ranked cards, followed by Card History Search and Pull History.

### Card Reference

- Full card reference for all six decks
- Upright and reversed meanings for both tarot decks
- Sailor Moon and Erotic Tarot translation tables
- African Goddess Rising cards organized by all 9 Temples
- Kimbition cards with reflective meanings, shadow themes, and lessons
- Heaven & Hell angel/demon pair system
- Deck-specific personal card notes
- Favorites system
- Clickable card modals
- In-page deck, suit, and temple filtering within long deck pages
- Expanded source-reference content with improved spacing

### Deck-Specific Meanings and Source References

Version 14 builds on the deck-specific reference system while keeping personal notes separate from published and source-based meanings.

The application includes:

- Sailor Moon source-reference meanings
- Erotic Tarot source-reference meanings and keyword chips
- African Goddess Rising source-reference fields
- Kimbition source-reference fields
- Heaven & Hell angel/demon light and shadow meanings audited against the provided source PDF
- Romantic Lenormand guidebook-based meanings, keywords, polarity, and supported timing associations
- Deck-specific personal notes stored locally

Shared card names remain separated by deck so notes, statistics, and reference context do not merge incorrectly.

### Card Lookup

- Search across all six decks
- Filter results by deck
- Search by card name, alternate name, theme, and meaning
- Keyword search for African Goddess Rising, Kimbition, Erotic Tarot, and Romantic Lenormand cards
- Lenormand reference filters for card number, name, meaning, keywords, and polarity
- Matching keywords display beneath relevant search results
- Erotic Tarot keyword chips derived from each card's Core Erotic Function
- Index-based modal opening for safer rendering of card data containing apostrophes

Example thematic searches include:

- `water`
- `healing`
- `shadow`
- `power`
- `desire`

### Spread Logger

- Log spreads with a date, name, question, tags, and overall synthesis
- Add cards from any of the six decks
- Use dedicated Tarot/Oracle and Lenormand tracker views
- Record positions and card-level notes in pull order
- Tarot and Oracle orientation options include Upright, Reversed, Sideways, and Unclear
- Lenormand entries use upright-only card meanings and omit orientation data
- Lenormand readings support positional or continuous-sentence interpretation, categories, and reflections
- Add custom section headers
- Reorder cards and sections
- Duplicate card rows for faster entry
- Edit previous spreads
- Clone spreads without duplicating the original synthesis

### Spread Templates

The application includes reusable templates for common reading structures, including:

- Three-card spreads
- Celtic Cross
- Ancestral Council
- Soul Map
- Future Spouse spread
- Sectioned custom layouts

Lenormand quick templates include single card, three-card line, five-card line, nine-card box, Grand Tableau (8 × 4 + 4), and custom spreads. Fixed layouts validate the expected card count, and custom layouts support mixed-deck readings.

Templates can use either a simple position array or grouped sections.

```js
{
  name: "My Template",
  sections: [
    { name: "Section One", positions: ["Card 1", "Card 2"] },
    { name: "Section Two", positions: ["Card 3"] }
  ]
}
```

### Tagging

The spread logger includes 23 tags:

`Love` · `Shadow` · `Career` · `Spirit` · `Body` · `Ancestors` · `Timing` · `General` · `Fun` · `Social` · `Travel` · `Fantasy` · `Erotic` · `Grief` · `Money` · `Health` · `Past` · `Future` · `Dream` · `🔎 Check-In` · `🧭 Decision` · `🗓️ Forecast` · `🕯️ Deity`

Tags can be combined with deck filters, sorting, and free-text search.

### Pull History

- Search across spread names, questions, cards, positions, notes, decks, and tags
- Filter by deck in the Tarot/Oracle tracker
- Dedicated Lenormand history with its own reading filter
- Filter by tag
- Sort by newest, oldest, most cards, or least cards
- Pagination with 8 spreads per page
- Click a saved spread to open a dedicated detail pop-up
- View spread name, question, date, tags, cards, positions, orientations, notes, and synthesis
- Edit, clone, and delete controls remain separate from the detail pop-up
- Collapsible sections within grouped spreads

### Statistics

- Total spread count for the selected tracker
- Per-deck spread counts
- Most Pulled Cards
- Upright and reversed percentages
- Orientation breakdown bars with an Other category for Sideways and Unclear cards
- Gold styling for the Other orientation category
- Lenormand top-eight ranked cards with positive, negative, or neutral polarity
- Separate Birds and Owls frequency counts
- Lenormand polarity totals and card frequencies by reading category
- Ordered combination frequencies and links to related readings
- Card History Search
- Spread-by-spread appearance history for individual cards

Personal card notes and favorites use deck-specific identifiers (`deck::cardname`). The current Tarot/Oracle frequency ranking groups identical card names, which remains a limitation for shared Major Arcana names.

### Data Management

All user data is stored in browser `localStorage`.

| Key | Contents |
|---|---|
| `marcyDeckPulls` | Logged spread data |
| `marcyCardNotes` | Deck-specific personal card notes |
| `marcyFavoriteCards` | Favorited card keys |
| `marcyOpenPulls` | Expanded pull-history entries |
| `marcyDeckMeanings` | Personal deck-specific meanings |
| `marcyLenormandCombinations` | Editable ordered combination interpretations |
| `marcyDeckTheme` | Light/dark theme preference |

The application also supports:

- Version 14 JSON export including readings, card notes, personal meanings, favorites, combination interpretations, and theme
- JSON import with support for earlier backups
- Full data clearing
- Offline use
- Browser-session persistence
- Persistent light/dark theme preference

### Interface and Navigation

- Light and dark mode
- Persistent theme preference
- Floating theme toggle in the bottom-left corner
- Sticky navigation
- Deck and suit navigation filters content in place instead of jumping down the page
- **All** buttons restore full deck views
- Improved spacing between card meaning sections
- Theme-aware modals, forms, tags, badges, search controls, and spread panels

## Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript
- DOM manipulation
- Browser localStorage
- JSON
- Git
- GitHub
- GitHub Wiki
- Responsive web design

The project has:

- No framework
- No package manager
- No build step
- No server
- No external runtime dependencies
- No required account
- No internet requirement after download

## Getting Started

### Option 1: Open Locally

1. Download the full application HTML file.
2. Open it in Chrome, Firefox, Safari, or Edge.
3. Begin browsing decks or logging spreads.

No installation is required.

### Option 2: Clone the Repository

```bash
git clone https://github.com/kingnihilism/Tarot-Grimoire.git
cd Tarot-Grimoire
```

Open the application HTML file in a modern browser.

## First-Time Use

### Browse the Decks

Use the navigation bar to open any deck page. Within long deck references, use the deck, suit, or temple filters to display only the section you want without jumping around the page.

### Add Personal Notes

Click a card to open its modal. Personal notes save automatically in the browser.

### Log a Spread

1. Open **Pull Tracker** for Tarot/Oracle or **Lenormand Pull Tracker** for Lenormand.
2. Choose a quick template or add cards manually.
3. Add sections when needed.
4. Select the deck, card, and optional position. Assign orientation for Tarot/Oracle cards.
5. Add notes, tags, and, for Lenormand, a reading style, category, and reflections.
6. Write an overall synthesis and save the spread.
7. Open the relevant Pull History to view, edit, or duplicate it.

### Back Up Your Data

Use **Export Data** regularly and store the JSON backup somewhere safe.

Because data is tied to the current browser, clearing browser storage or opening the application on another device will not automatically transfer your entries.

## Deck Translations

### Sailor Moon Tarot

| Sailor Moon | Standard Tarot |
|---|---|
| Crescent | Cups |
| Talisman | Swords |
| Rods | Wands |
| Crystals | Pentacles |
| Guardian | Knight |
| Maiden | Page |
| Princess | Queen |
| Queen | King |

### Erotic Tarot

| Erotic Tarot | Standard Tarot |
|---|---|
| Shells | Cups |
| Feathers | Swords |
| Candles | Wands |
| Roses | Pentacles |
| The Awakening | Judgement |
| The High Priest | The Hierophant |

## Project Structure

The application is intentionally maintained as a lightweight front-end project.

```text
Tarot-Grimoire/
├── index.html
├── README.md
├── quickstart.html
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
└── _config.yml
```

Within the application file:

- **CSS** defines the visual system and responsive components
- **HTML** defines the application sections and interface
- **Data objects** store card, deck, and spread-template information
- **JavaScript functions** manage rendering, persistence, filtering, statistics, and interactions

## Technical Decisions

### Vanilla JavaScript

The project uses vanilla JavaScript to strengthen understanding of:

- State management
- DOM updates
- Event handling
- Data transformation
- Search and filtering logic
- Browser persistence
- Debugging without framework abstractions

### Single-File Application

The single-file format makes the project easy to download, open, back up, and use offline.

The tradeoff is that the file becomes harder to maintain as features grow. A future version may separate data, styles, and logic into individual files.

### Local-First Storage

localStorage keeps the application private and easy to use without authentication or hosting infrastructure.

The tradeoff is that data does not automatically sync across browsers or devices.

## Version 14 — Romantic Lenormand Expansion

- Sixth deck with 37 searchable profiles, including distinct Birds and Owls entries
- Expanded personal deck profile describing the six-deck reading system
- Dedicated Lenormand Pull Tracker with manual, ordered card entry and six quick templates
- Upright-only logging, guidebook polarity, source references, and personal notes
- Ranked card frequencies, polarity totals, category statistics, and editable combination encyclopedia
- Matching tracker layouts with searchable card histories and editable, paginated reading histories
- JSON backup support for Lenormand reading metadata, combinations, and theme

## Version 12 Highlights

### Added

- Light and dark mode with persistent theme preference
- Floating theme toggle
- Pull History detail pop-ups
- Four new spread tags: 🔎 Check-In, 🧭 Decision, 🗓️ Forecast, and 🕯️ Deity
- Sideways and Unclear card orientations
- Gold styling for the Other orientation category
- Erotic Tarot keyword chips and Card Lookup keyword matching
- Expanded source-reference content across the five-deck system

### Improved

- Deck, suit, and temple navigation now filters content in place instead of using page jumps
- Card meaning sections have improved spacing for readability
- Pull History browsing is separated from Edit, Clone, and Delete controls
- Orientation statistics no longer treat Sideways or Unclear cards as Upright
- Heaven & Hell angel/demon pairings and concise light/shadow meanings were audited against the provided PDF
- Source-reference explanations no longer display trailing citation-style numbers
- Theme styling is consistent across navigation, modals, forms, tags, badges, search controls, and spread panels

See [CHANGELOG.md](CHANGELOG.md) for the full project history.

## Documentation

The GitHub Wiki documents the application, including:

- Architecture
- Card data models
- Deck system (original five-deck documentation)
- Spread logger
- Spread templates
- Search and filtering
- Statistics
- Data management
- User interface and responsive design
- Technical decisions
- Known limitations
- Troubleshooting
- Contributing
- Version history

## Skills Demonstrated

- Front-end web development
- JavaScript programming
- Data modeling
- Dynamic form generation
- Search and filtering logic
- Browser storage
- JSON serialization
- Responsive interface design
- Debugging
- Feature iteration
- Version control
- Technical writing
- Project documentation
- Independent project planning

## Known Limitations

- Data is tied to the current browser and device
- Clearing browser storage deletes local data unless it was exported
- There is no cloud sync or user authentication
- The growing single-file architecture may become harder to maintain
- There is no automated test suite in the repository
- Tarot/Oracle card frequency rankings can combine identical card names across decks
- Deck content remains dependent on manually maintained data objects and source-reference updates

## Future Improvements

Potential future work includes:

- Refactoring the single file into separate modules
- Automated testing
- Optional cloud synchronization
- Improved accessibility auditing
- Additional statistics and visualizations
- More customizable spread templates
- Expanded data validation during import
- Better mobile form controls

## Contributing

This is a personal project, but the repository includes a contributing guide explaining its structure, data formats, and development workflow.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This project is for personal and portfolio use.

Deck names, artwork, characters, and published card content belong to their respective creators and publishers.
