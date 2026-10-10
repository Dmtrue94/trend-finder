# Trend Finder

Describe your app, press one button, and see what is growing on TikTok and Instagram in the USA, UK and Canada right now, with numbers and a ready video idea for each trend.

Made for app marketers who look for creative angles in what their audience cares about this week.

## Use it

1. Open the site.
2. Write a few words about your app.
3. Paste your Anthropic API key (get one at console.anthropic.com). It stays in your browser and goes only to Anthropic. A search costs a few cents on your key.
4. Press **Find trends**.

No key? Press **Copy request for Claude**, paste it into a new Claude chat and send it. The request already has this week's trend data inside.

## Don't want to paste your key into a website?

Fair. Run it on your own computer instead:

1. Download the ZIP: https://github.com/Dmtrue94/trend-finder/archive/refs/heads/main.zip
2. Unzip it and double-click `index.html`. It opens in your browser.
3. Paste your key and press **Find trends**.

Nothing to install. The key is sent only to `api.anthropic.com`, and you can check that yourself: the only `fetch` call in `index.html` goes there. Download the ZIP again any day to get fresh trend data.

Extra safety: create a separate key just for this tool, set a monthly spend limit in the Anthropic Console, and delete the key whenever you want.

## What you get

For each trend: how hot it is and how long you have, what is happening, why it fits your app, numbers with links, a video idea second by second, other first lines, and what to avoid. Plus what was skipped and why.

## How it works

- The whole site is one file: `index.html`. No server, no database.
- This week's trend data sits inside the page. It is collected once a day from TikTok Creative Center (top hashtags by country, with how they moved during the week) and from public Instagram videos. Only numbers and links are kept.
- A hashtag counts as growing when the end of its week is clearly higher than the start and the last day is high. Hashtags that peaked mid-week or fell are skipped.
- Your search sends your app description and the trend data to Claude with your own key, straight from your browser.

## Your own copy

Put `index.html` on any static hosting: Vercel, Netlify or GitHub Pages. Nothing to configure.

## Note on data

Data comes from public pages. Whoever runs a copy is responsible for following the rules of TikTok and Instagram.

## License

MIT
