# Clear Heatmap: NSE Heatmap Redesign

A responsive web application that redesigns the NSE India Broad Market Indices heatmap so that it is easier to read, search and filter.

**Benchmark website:** https://www.nseindia.com/market-data/live-market-indices/heatmap
**Live application:** [insert your GitHub Pages link]

## Problem Statement

Beginners and mobile users find the NSE index heatmap hard to use because some tile names are cut off, gain and loss are shown mainly through colour, and the heatmap has no quick way to search, sort or filter the indices.

How might we make the NSE index heatmap easier to read, search and understand for beginners, including on small screens?

## Target Users

- College students learning about the stock market
- New investors who want a quick overview of market segments
- Mobile users who check the market briefly

## Features

- Full index names on tiles (text wraps instead of being cut off)
- Arrows (up and down), signed percentages and a plain-text legend, so meaning does not depend on colour alone
- Live search by index name
- Sorting: best performing, worst performing, or A to Z
- Gainers / Losers / All filter
- Heatmap view and table view with a Status column
- "No data" label for missing values
- Loading, empty-result and error messages
- Responsive layout for phone, tablet and desktop

## Technologies

- HTML5
- Tailwind CSS (CDN)
- JavaScript (ES6)
- Fetch API
- JSON
- Git and GitHub Pages

## JavaScript Events Used

| Event | Element | Purpose |
|---|---|---|
| `input` | Search box | Filters tiles as the user types |
| `change` | Sort dropdown | Re-sorts the indices |
| `click` | Gainers / Losers / All buttons | Filters tiles |
| `click` | View button | Switches between heatmap and table |

## How It Works

1. `fetch("data.json")` requests the index data.
2. `response.json()` converts it to JavaScript objects.
3. `render()` filters, sorts and draws the tiles or table.
4. If `data.json` cannot be fetched (for example when the file is opened by double-click), a built-in copy of the same data is used and the user is told.

## Project Structure

```
nse-heatmap-redesign/
├── index.html
├── data.json
└── README.md
```

## How to Run

1. Download or clone this repository.
2. Open `index.html` in a browser with an internet connection (needed for the Tailwind CDN).
3. Or open the live link above.

## Testing

Tests were performed manually. Summary:

| Test | Result |
|---|---|
| Page load shows tiles and status message | [fill after testing] |
| Search "smlcap" shows only small-cap indices | [fill after testing] |
| Search "zzz" shows empty-state message | [fill after testing] |
| Sort best / worst / name | [fill after testing] |
| Gainers, Losers and All filters | [fill after testing] |
| Table view | [fill after testing] |
| Mobile layout | [fill after testing] |
| Fetch failure shows fallback message | [fill after testing] |

## Limitations

- The data is a **sample snapshot** copied from the NSE heatmap page on 15-Oct-2026 (13:28:54 IST). It is not live market data.
- Only Broad Market Indices are included.
- Tailwind is loaded from a CDN, which suits a prototype but not production.
- This is a student prototype and must not be used for trading decisions.

## Future Improvements

- Connect to an authorised live data source
- Add Sectoral, Thematic and Strategy indices
- Add a colour-blind-friendly mode
- Add a trend chart for each index

## Author

[Your name] | [Roll number] | [Course]
