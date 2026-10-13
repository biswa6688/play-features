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
| Environment / .env Configuration Migration (PlayService) | [`env-config-migration/`](env-config-migration/index.html) | PlayService's `PLAY_SYS_*` env var rename, Nucleus-first config resolution, removed local-DB-config mode, and the new graceful shutdown timeout. |
| PlayWeb Host Runtime Configuration | [`playweb-runtime-config/`](playweb-runtime-config/index.html) | PlayWeb's backend addresses, app code, credentials, and encryption key now served dynamically from `host/.env` at page load, plus the new dev/production runtime switch. |
| Session Data APIs | [`session-data-apis/`](session-data-apis/index.html) | `GET /play-api/{ai-rating,ratings,sentiment,summary,transcripts}-bysession/:xsessid` — how to call each endpoint, what it returns, and its error cases. |
| Transcript Translation | [`translation/`](translation/index.html) | Translating a call, video or chat transcript into any language from a searchable list, with a tab per language, download and remove. |
| Agent and Customer Wise Questions | [`agent-customer-questions/`](agent-customer-questions/index.html) | Rating versions with a User Type (Agent, Customer or Both), the version menu tree, and the Customer / per-agent tabs on the Ratings tab. |
| Keywords and Aliases | [`keyword-aliases/`](keyword-aliases/index.html) | Adding process keywords with aliases (any language) that are counted together in the recording summary, with entry shortcuts and limits. |
| Media Decryption with Keys | [`media-decryption/`](media-decryption/index.html) | Saving an encryption key per channel, switching Encryption on, and how encrypted recordings are unlocked in the browser and played; error messages explained. |
| Voice Percentage Detection | [`voice-percentage-detection/`](voice-percentage-detection/index.html) | How PLAY measures how much of a call or video recording is speech before generating a transcript — FFmpeg prepares the sound, Silero VAD scores it, the minimum speech ratio setting, and what you see when a recording is too quiet. |

When adding a new feature folder here, add a row to this table.
