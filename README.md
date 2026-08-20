# PLAY-Features

Standalone HTML documentation for individual PLAY features. Each feature gets its own folder: `index.html` (links out, no inline styles), `css/style.css`, and `favicon.ico` (copied from `playweb4.x/public/icons/favicon.ico`).

## Features

| Feature             | Folder                                                   | Description                                                                                                                            |
| ------------------- | --------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| AI Criteria         | [`ai-criteria/`](ai-criteria/index.html)                 | Configuring per-answer AI grading criteria on process version questions.                                                               |
| Sentiment Gradient  | [`sentiment-gradient/`](sentiment-gradient/index.html)   | How the customer sentiment ring (Summary page) and customer/agent bars (Sentiment Analysis page) render a per-sentence color gradient. |
| Record Media Lookup | [`record-media-lookup/`](record-media-lookup/index.html) | `GET /play-api/record-media/:campaign/:channel` — single-recording lookup vs. paged listing, the limit/offset/includecount params, and the fromdate/todate date filter. |
| Rating Score Calculation | [`rating-score-calculation/`](rating-score-calculation/index.html) | How an AI rating's `totalScore` is calculated — category/question/answer weightage, and how N/A answers are renormalized within a category and across categories. |
| Response Headers Configuration (PlayService) | [`response-headers-config-playservice/`](response-headers-config-playservice/index.html) | `.env`-driven CORS and security response headers, and stripping headers like `X-Powered-By`, on the PlayService API server. |
| Response Headers Configuration (PlayWeb) | [`response-headers-config-playweb/`](response-headers-config-playweb/index.html) | `.env`-driven CORS and security response headers, and stripping headers like `X-Powered-By`, on the PlayWeb host server. |

When adding a new feature folder here, add a row to this table.
