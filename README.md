# Days Left Visualizer

A minimalist, configurable web app that visualizes days between two dates as an interactive dot grid. Meant for tracking progress through time-boxed experiences.

- Interactive dot grid showing past, present, and future days
- Progress bar with percentage completion
- Special day highlighting with hover descriptions
- Support for excluded date ranges (e.g., holidays, breaks)
- Weekend exclusion option
- Configurable title, subtitle, and favicon
- Markdown link support in subtitle text
- Fully client-side with no dependencies
- Configuration saved to local storage
- Download configured HTML for offline use

## Usage

1. Download `index.html`
2. Open it in a web browser
3. Click "edit config" to customize:
   - Set start and end dates
   - Add special days with descriptions
   - Define excluded date ranges
   - Customize title and subtitle
   - Toggle weekend exclusion
   - Change the favicon emoji

### Configuration Format

```json
{
  "title": "Your Title",
  "subtitle": "Supporting text with optional [markdown links](https://example.com)",
  "favicon": "📅",
  "startDate": "YYYY-MM-DD",
  "endDate": "YYYY-MM-DD",
  "excludedRanges": [
    {
      "start": "YYYY-MM-DD",
      "end": "YYYY-MM-DD",
      "label": "Description of excluded period"
    }
  ],
  "excludeWeekends": true,
  "specialDays": {
    "YYYY-MM-DD": "Description of special day"
  }
}
```

## Visual Guide

- 🔵 Blue dots: Past days
- 🟢 Light green dots: Future days
- 🟡 Yellow dot: Today
- ⬛ Dark green squares: Special days
- ⚪ Outlined dots: Excluded days

## Keyboard Shortcuts

- `Ctrl/Cmd + S`: Download configured HTML file

## Credits

Inspired by:
- ["Day by Day"](https://days.rory.codes/) by Rory Flint ([ruairidhflint/day-by-day](https://github.com/ruairidhflint/day-by-day))
- ["Your Life in Weeks"](https://waitbutwhy.com/2014/05/life-weeks.html) from Wait But Why
