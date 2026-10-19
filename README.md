# English Poetry Meter Scansion Analyzer

A browser-based tool to analyze the metrical structure of English poetry.

## Features

- **Syllabification**: Splits each word into syllables using vowel-cluster detection, silent-e rules, and common suffix handling (-ed, -tion, -ing)
- **Automatic stress assignment**: Applies an iambic stress pattern by default across the whole line
- **Meter identification**: Detects iambic, trochaic, dactylic, anapestic, spondaic, and pyrrhic patterns; identifies Iambic Pentameter, Tetrameter, Trimeter, etc.
- **Visual scansion**: Yellow = stressed (/), blue = unstressed (u); foot boundaries marked with |
- **Manual override**: Click any syllable to toggle its stress — the meter summary updates instantly
- **Line-by-line table**: Shows pattern string, syllable count, feet count, and meter per line
- **3 built-in presets**: Shakespeare Sonnet 18, Robert Frost's The Road Not Taken, Emily Dickinson's Because I could not stop for Death

## Usage

1. Open `index.html` in any modern browser
2. Paste or type a poem in the text area
3. Click **Analyze**
4. Click any syllable in the scansion view to toggle its stress
5. Use the preset buttons to load famous examples

## Technical Notes

- No server required — fully static
- No external API calls (only Tailwind CSS CDN)
- No data persistence needed
- XSS-safe: all user text is HTML-escaped before insertion
- Accessible: ARIA labels on all interactive syllable spans
