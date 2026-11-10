# Jeff Winter Event Scraper

A small web tool built for a client's newsletter. It collects recent news about Industry 4.0 and manufacturing events in one place, so the client can pick the stories they want and write them up, instead of searching for them by hand each week.

Live: [jeff-newsletter-tool.netlify.app](https://jeff-newsletter-tool.netlify.app/)

## How it works

- The user picks keyword categories such as "smart manufacturing conference" or "IIoT conference", and a time window of 7 or 30 days.
- A Netlify Function searches Google News RSS for each keyword, reads the top 10 results per keyword, removes duplicates and sorts them newest first.
- The results can be searched, sorted by date, source or title, and ticked to add them to a write-up queue.
- In the queue, the client adds a headline and commentary for each post.
- The queue downloads as an Excel file with the title, source, date, keyword, notes, write-up and link for each post.

## Tech

- HTML, CSS and JavaScript (no framework)
- Netlify Functions (Node.js) with `fast-xml-parser`
- SheetJS for the Excel export
- Google News RSS as the data source

## Run it locally

The scraper runs as a Netlify Function, so use the Netlify CLI:

```bash
npm install
npx netlify-cli dev
```

---

Ahmed Amine Tiffrent · [Portfolio](https://www.aminetiffrent.com/portfolio)
