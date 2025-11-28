# Global Unicorns Dashboard

An interactive data visualization dashboard exploring the CB-Insights Global Unicorn Club dataset (October 2025), featuring 1,331 unicorn companies valued at $5.2 trillion.

## Overview

This single-page dashboard presents comprehensive analysis of the global unicorn ecosystem through 7 thematic sections with 24 interactive charts built with D3.js v7.

## Features

- **Executive Overview**: KPI cards and treemap of top 20 unicorns by valuation
- **Geographic Analysis**: Country rankings, regional distribution (radial bar chart), and scatter analysis
- **Industry Breakdown**: Marimekko chart combining count and valuation, average valuations, country breakdown
- **Temporal Analysis**: Year-over-year trends, industry evolution, cumulative growth
- **City & Hub Analysis**: Circle packing visualization, city valuations, US vs China comparison
- **Investor Intelligence**: Top investors, pictogram array of investor types, diversification analysis
- **Valuation Distribution**: Beeswarm plot, value concentration, industry ranges

## Technical Stack

- **Visualization**: D3.js v7 (CDN)
- **Styling**: Electric Dark theme with CSS variables
- **Data**: Embedded JSON (no external dependencies)
- **Layout**: Responsive 2x2 grid sections

## Usage

Simply open `index.html` in a modern web browser. No server required.

```bash
# Option 1: Direct file open
open index.html

# Option 2: Local server (optional)
python3 -m http.server 8080
```

## Interactive Filters

- **Country**: Filter by specific country or view all
- **Industry**: Filter by sector (Enterprise Tech, Financial Services, etc.)
- **Year Range**: Adjust the time period for analysis

## Chart Types

| Visualization | D3 Method | Section |
|--------------|-----------|---------|
| KPI Cards | DOM manipulation | Executive |
| Treemap | d3.treemap() | Executive |
| Horizontal Bar | d3.scaleBand() | Geographic, Cities |
| Radial Bar | d3.arc() + scaleBand() | Geographic |
| Doughnut/Pie | d3.arc() + d3.pie() | Various |
| Scatter/Bubble | d3.scaleLinear() | Geographic, Cities |
| Marimekko | Custom layout | Industry |
| Line/Area | d3.line() + d3.area() | Temporal |
| Stacked Bar | d3.stack() | Industry, Temporal |
| Circle Packing | d3.pack() | Cities |
| Pictogram Array | Custom grid | Investors |
| Beeswarm | d3.forceSimulation() | Valuation |

## Data Source

CB-Insights Global Unicorn Club (as of October 7th, 2025)
- 1,331 unicorn companies
- 56 countries, 308 cities
- 7 industry sectors
- Total valuation: $5.2 trillion

## Color Palette

```css
--lime: #BEFF00      /* Primary accent */
--cyan: #00BAFE      /* Enterprise Tech, North America */
--amber: #FFC000     /* Financial Services, Asia */
--emerald: #00DE71   /* Consumer & Retail, Europe */
--coral: #F04E50     /* Healthcare, alerts */
```

## Browser Support

Tested on modern browsers (Chrome, Firefox, Safari, Edge). Requires JavaScript enabled.

## License

Data source: CB-Insights. Visualization by Aref.
