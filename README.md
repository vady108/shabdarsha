# shabdarsha.com

A tiny daily-quote website — one motivational quote a day, plus a shuffle for a
word at random. Static, no build step, hosted on GitHub Pages.

## Structure
- `index.html` — the whole site (inline CSS + JS).
- `quotes.js` — the quote collection. **To add a quote, append a `{ text, author }`
  object to the `window.QUOTES` array** and push; the site picks it up automatically.
- `CNAME` — custom domain (`shabdarsha.com`).

## How the "quote of the day" works
The featured quote is chosen deterministically from the calendar day-of-year, so
every visitor sees the same quote on a given day and it rotates daily on its own.
"New quote" shuffles randomly (client-side); "Today's quote" returns to the daily pick.

## Hosting
GitHub Pages, served from the `main` branch. Custom domain via the `CNAME` file plus
DNS records at the registrar (apex A records to GitHub Pages + `www` CNAME).
