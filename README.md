# proton-birthday-calendar-adapter
Import your Google/Outlook contacts to make a Proton birthday calendar

**Use it here: https://fulldecent.github.io/proton-birthday-calendar-adapter/**

## How it works

1. Export your contacts as CSV from [Google Contacts](https://contacts.google.com/) (Export → Google CSV) or [Outlook](https://outlook.live.com/people/) (Manage contacts → Export contacts).
2. Drop the CSV file onto the page (or click to choose it).
3. Download `birthdays.ics` and import it in Proton Calendar (Settings → Import).

Each contact with a birthday becomes a yearly, all-day event named "FNAME LNAME birthday". Supported birthday formats include `1934-01-26`, `--03-17` (no year), `FEB 29`, `February 29, 1990`, and Outlook's `1/26/1934`. February 29 birthdays are shown on February 28 every year, with a note that the birthday is actually on February 29.

Everything runs locally in your browser in a single self-contained [`index.html`](index.html) with zero external dependencies; your contacts are never uploaded.

## Publishing

The [Deploy to GitHub Pages](.github/workflows/pages.yml) workflow publishes `index.html` on every push to `main`. If Pages is not yet enabled, go to Settings → Pages and set **Source** to **GitHub Actions**.
