# 🌿 Marcy's Deck Grimoire

A browser-based tarot and oracle reference, spread logging, and pattern-tracking application built with **HTML, CSS, and vanilla JavaScript**.

The project supports a five-deck practice with different card structures, meanings, and roles while remaining fully offline. It includes searchable card references, customizable spread logging, deck-specific notes and meanings, statistics, filtering, JSON backups, and a documented GitHub Wiki.

## Live Project

- **Repository:** https://github.com/kingnihilism/Tarot-Grimoire
- **Wiki:** https://github.com/kingnihilism/Tarot-Grimoire/wiki
- **Current Version:** v11

## Project Goals

Marcy's Deck Grimoire was created to solve several practical problems:

- Keep five different tarot and oracle systems in one searchable reference
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

## Features

### Card Reference

- Full card reference for all five decks
- Upright and reversed meanings for both tarot decks
- Sailor Moon and Erotic Tarot translation tables
- African Goddess Rising cards organized by all 9 Temples
- Kimbition cards with reflective meanings, shadow themes, and lessons
- Heaven & Hell angel/demon pair system
- Deck-specific personal card notes
- Favorites system
- Clickable card modals
- Jump navigation within long deck pages

### Deck-Specific Major Arcana Meanings

Version 11 adds editable upright and reversed meanings for Major Arcana cards in the Sailor Moon and Erotic Tarot decks.

These meanings:

- Are stored separately for each deck
- Use the `marcyDeckMeanings` localStorage key
- Persist between browser sessions
- Are included in JSON export and import
- Are cleared with the application's clear-data controls

This prevents shared Major Arcana names from losing their deck-specific context.

### Card Lookup

- Search across all five decks
- Filter results by deck
- Search by card name, alternate name, theme, and meaning
- Keyword search for African Goddess Rising and Kimbition cards
- Matching keywords display beneath relevant search results
- Index-based modal opening for safer rendering of card data containing apostrophes

Example thematic searches include:

- `water`
- `healing`
- `shadow`
- `power`
- `desire`

### Spread Logger

- Log spreads with a date, name, question, tags, and overall synthesis
- Add cards from any of the five decks
- Record position, orientation, and card-level notes
- Add custom section headers
- Reorder cards and sections
- Duplicate card rows for faster entry
- Edit previous spreads
- Clone spreads without duplicating the original synthesis
- Expand and collapse logged entries

### Spread Templates

The application includes reusable templates for common reading structures, including:

- Three-card spreads
- Celtic Cross
- Ancestral Council
- Soul Map
- Future Spouse spread
- Sectioned custom layouts

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

The spread logger includes 19 tags:

`Love` · `Shadow` · `Career` · `Spirit` · `Body` · `Ancestors` · `Timing` · `General` · `Fun` · `Social` · `Travel` · `Fantasy` · `Erotic` · `Grief` · `Money` · `Health` · `Past` · `Future` · `Dream`

Tags can be combined with deck filters, sorting, and free-text search.

### Pull History

- Search across spread names, questions, cards, positions, notes, decks, and tags
- Filter by deck
- Filter by tag
- Sort by newest, oldest, most cards, or least cards
- Pagination with 8 spreads per page
- Expand and collapse spread entries
- Collapsible sections within grouped spreads
- Edit and clone existing entries

### Statistics

- Total spread count
- Per-deck card counts
- Most Pulled Cards
- Upright and reversed percentages
- Orientation breakdown bars
- Card History Search
- Spread-by-spread appearance history for individual cards

Cards with matching names across decks are keyed using:

```text
deck::cardname
```

This prevents Sailor Moon and Erotic Tarot Major Arcana statistics and notes from merging incorrectly.

### Data Management

All user data is stored in browser `localStorage`.

| Key | Contents |
|---|---|
| `marcyDeckPulls` | Logged spread data |
| `marcyCardNotes` | Deck-specific personal card notes |
| `marcyFavoriteCards` | Favorited card keys |
| `marcyOpenPulls` | Expanded pull-history entries |
| `marcyDeckMeanings` | Deck-specific Major Arcana meanings |

The application also supports:

- JSON export
- JSON import
- Full data clearing
- Offline use
- Browser-session persistence

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

Use the navigation bar to open any deck page. Each page includes its own reference content, deck profile, and navigation tools.

### Add Personal Notes

Click a card to open its modal. Personal notes save automatically in the browser.

### Log a Spread

1. Open **Pull Tracker**
2. Choose a template or add cards manually
3. Add sections when needed
4. Select each deck, card, position, and orientation
5. Add notes and tags
6. Write an overall synthesis
7. Save the spread

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
├── application HTML file
├── README.md
├── QUICKSTART.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── .gitignore
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

## Version 11 Highlights

### Added

- Editable deck-specific upright and reversed meanings for Sailor Moon and Erotic Tarot Major Arcana
- Separate `marcyDeckMeanings` localStorage persistence
- Deck-specific meanings in JSON export, import, and clear-data operations
- AGR and Kimbition keyword matching in Card Lookup
- Visible matching keywords beneath search results

### Improved

- Standardized card-list modal behavior through `openModalByIndex`
- Improved thematic search discoverability
- Strengthened separation of shared card names across decks

See [CHANGELOG.md](CHANGELOG.md) for the full project history.

## Documentation

The GitHub Wiki contains 16 connected pages covering:

- Architecture
- Card data models
- Five-deck system
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
- The application does not currently include automated tests
- Deck content remains dependent on manually maintained data objects

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
- Optional theme settings

## Contributing

This is a personal project, but the repository includes a contributing guide explaining its structure, data formats, and development workflow.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This project is for personal and portfolio use.

Deck names, artwork, characters, and published card content belong to their respective creators and publishers.
