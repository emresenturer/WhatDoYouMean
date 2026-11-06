# What Do You Mean

A communication analyzer for the texts you keep re-reading at 2am. Paste a conversation. Choose how you want to be talked to. Get insight that respects your intelligence, and your privacy.

**Live:** https://emresenturer.github.io/WhatDoYouMean/

## What it does

Paste a text conversation, optionally say which speaker is you, and pick a feedback style: **Straight talk**, **Gentle**, **Analytical**, or **Like a friend**. You get:

1. **What they most likely mean**, with 2 to 3 alternative readings and how likely each one is
2. **Tone and emotional temperature**, on a cold to heated scale
3. **What is NOT in the message**, so you do not over-read it
4. **Your part**: how your own messages may be landing
5. **Suggested replies**: three, in different tones, each with a copy button
6. **When to just ask directly**, with a natural way to ask

Copy the whole analysis or download it as Markdown. A **Try a sample** button loads an example conversation.

### What it will not do

It does not diagnose anyone or label people (no "narcissist", "manipulative", and so on), and it does not give clinical advice. If a conversation suggests danger or self-harm, it shows a short line pointing to real help (local emergency services, 988 in the US, or findahelpline.com elsewhere).

## Privacy

- Nothing you paste is stored. The conversation goes from your browser directly to `api.anthropic.com` and is gone when you press **Clear everything** or close the tab.
- The only thing saved is your Anthropic API key, in this browser's `localStorage` (`whatdoyoumean_anthropic_key`). **Forget** removes it.
- No server, no analytics, no cookies.

## Bring your own key

You need an Anthropic API key: https://console.anthropic.com/settings/keys. Usage is billed to your own Anthropic account. The app calls the Messages API with model `claude-opus-5-5`.

## Run locally

```bash
git clone https://github.com/emresenturer/WhatDoYouMean.git
cd WhatDoYouMean
python3 -m http.server 8000
# open http://localhost:8000
```

## Stack

A single `index.html`: plain HTML, CSS, and JavaScript. No build step, no dependencies, no framework. Fonts from Google Fonts. Deployed with GitHub Pages from `main` (root).

## License

MIT, Emre Senturer, 2026.
