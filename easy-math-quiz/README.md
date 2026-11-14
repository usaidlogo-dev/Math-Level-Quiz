# Easy Math Level Quiz – Score Checker

A free, mobile-first, browser-only Grade 4 maths answer checker. Built with plain HTML, CSS and JavaScript. The answer key is bundled in `answers-data.js`; checking and progress storage happen in the browser.

## Run locally

You can open `index.html` directly, or run it from a local static web server. For example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## Deploy free

Upload the contents of this folder to a static host such as Netlify or Vercel. No build command is needed; the publish directory is this folder and the entry file is `index.html`.

## Included

- 10 chapters and 4 Final Challenge pages from the supplied answer key
- Local browser progress (`localStorage`)
- Child welcome step (first name, surname and age); profile details are not sent or persisted
- Score feedback, wrong-answer review and retry of incorrect answers
- Book overview, star thresholds, printable certificate and downloadable PDF result report
- Bundled answer key (no separate answer-file fetch or internet connection needed)
- Basic offline caching when hosted over HTTPS or localhost (service worker)

## Privacy / deployment note

The site itself sends no form data to a server and has no analytics, ads or external links. Static hosting will still serve the site files as normal web requests. Progress is saved on the current browser/device. Clearing site data clears progress. The answer key is shipped to the browser, so it is not secret; this is appropriate for a workbook companion checker, not for a secure exam.

## Important answer-checking note

Circle It checks the stored `letter` value. Numeric answers are not used for that section. For other sections, matching is case-insensitive and tolerant of spaces, commas, currency symbols, common measurement units, and common remainder notation. Multi-value numeric answers are compared without order.
