# heylaowang

The front page of **heylaowang.com** (老王｜经常爬山，也聊股票和 AI), as a static GitHub Pages site:
https://ryanlr.github.io/heylaowang/

It replaces the page that a CloudFront Function used to generate on every request. The HTML is
a byte-for-byte copy of that page (snapshot 2026-11-12), with only these changes:

- links to the two sections point straight at their GitHub Pages sites:
  `/ai/` → https://ryanlr.github.io/ai/ and `/stock_trading/` → https://ryanlr.github.io/stock_trading/
- the HEY 老王 brand link is relative (`./`)
- added a meta description, a canonical link to https://heylaowang.com/, and a matching 404 page

## Files

| File | |
|---|---|
| `index.html` | the front page (inline CSS, Google Analytics G-2G0J05CN16) |
| `404.html` | not-found page in the same style |
| `.nojekyll` | serve files as-is |

## Pointing heylaowang.com here

Today the CloudFront Function answers `/` with the page and 302-redirects `/ai/` and `/stock_trading/`
to their GitHub Pages sites. To retire the page from the function, change it to redirect `/` to
https://ryanlr.github.io/heylaowang/ (keep the `/ai/` and `/stock_trading/` redirects).
