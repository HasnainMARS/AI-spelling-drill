# AI Spelling Drill

A browser-based spelling and grammar practice tool for **IELTS**, **PTE Academic**, **PTE Academic UKVI**, and **PTE Core** test preparation. Single static HTML file, no build step, no dependencies — open it directly or host it anywhere.

## Features

- **Audio dictation drill** — hear a word read aloud (via the browser's built-in text-to-speech) and type what you heard, similar to the listening/dictation tasks on these tests.
- **Test format selector** — choose PTE Academic, PTE Academic UKVI, PTE Core, or IELTS, and your results are scored on that test's actual scale (10–90 scaled score, or 1–9 IELTS-style bands).
- **Practice and Exam modes** — Practice allows replays and hints; Exam plays the word once with a countdown timer, closer to real test conditions.
- **Voice accent picker** — Default, American, British, or Australian, since real listening sections use multiple native-English accents.
- **Custom word lists** — add your own words one at a time or in bulk, then drill yourself on just that list.
- **Progress tracking** — every round is saved with a chart of accuracy over time, a day streak, best score, and a session history.
- **AI grammar checker** — paste a sentence or short paragraph and get a corrected version with a tracked-change-style diff and short notes on what was fixed.
- **Share results** — share your score via the native share sheet or clipboard.

## Hosting

This is a single `index.html` file with everything (HTML, CSS, JS) inlined. To deploy:

1. Upload `index.html` to a static host — GitHub Pages, Netlify, Vercel, and Cloudflare Pages all have free tiers that work well for this.
2. No build step or server is required.

## Data storage

Your custom word list and progress history are saved in your own browser's local storage. That means your data is personal to whichever browser/device you're using — it isn't sent to a server, and it isn't shared with other visitors to the same deployed site.

## About the grammar checker

The grammar checker calls the Anthropic API to perform the actual correction. This works automatically when the app runs inside Claude.ai's artifact preview. If you self-host this file elsewhere, that feature needs its own backend holding a private API key (an API key should never be placed in client-side code, so one isn't included here). Without a backend in place, the grammar checker will show a friendly "not available right now" message rather than breaking the rest of the app — every other feature works fully standalone.

## Tech stack

Plain HTML, CSS, and JavaScript. No frameworks, no package manager, no build tools.

## Disclaimer

This is an independent practice tool inspired by the listening-and-spelling style tasks used in these tests. It is **not affiliated with or endorsed by** Pearson, IDP, the British Council, or Cambridge Assessment English.

## License

No license has been set yet — add one (e.g. MIT) if you want to make clear how others can use or modify this code.
