# 🎙️ Standup Analyzer — but for free, with surprise goodies

> Your standup meeting, analyzed in real-time. No account. No subscription. No Gong.

**[→ Open the app](https://assafbar2.github.io/standup-analyzer-but-for-free-with-surprise-goodies/)**

---

## What is this?

Standup Analyzer listens to your team's daily standup, transcribes it live in the browser, and streams an AI-powered breakdown as you speak — issues, blockers, action items, tickets, follow-ups, team mood, and a handful of surprise extras that make the whole thing actually fun.

When the meeting ends, you get a structured summary you can copy as Markdown and drop straight into Notion, Slack, or wherever your team lives.

---

## Why not just use Gong?

Gong is powerful. Gong is also:

- **$$$** — enterprise pricing, seat licenses, procurement cycles
- **Recording everything** — calls are uploaded to Gong's servers, transcribed there, stored there
- **Overkill for standups** — it's built for sales calls, not a 10-minute team sync
- **Another tool to log into** — with an admin, and a dashboard, and integrations to configure

This app is a single HTML file. You open it in Chrome. It listens to your mic using the browser's built-in speech API. The transcript is analyzed by Claude (via your own API key). Nothing leaves your machine except the text going to Anthropic's API — the same API your team probably already uses for other things.

No recording stored anywhere. No account. No seats. No renewals.

---

## Why a single HTML file?

Because the best tool is the one people actually use.

A single file means:
- **Zero setup** — open it, enter your API key once, start recording
- **Works offline-ish** — the file itself needs no server; only the AI call needs internet
- **Easy to self-host** — drop it on GitHub Pages, S3, or your own server
- **Easy to audit** — every line of code is visible in View Source; no bundled black boxes
- **Easy to fork** — change the prompt, add a category, reskin it in five minutes

Complex software stacks are how good ideas become shelfware. This stays simple on purpose.

---

## The surprise goodies

Beyond the standard meeting analysis, there's a "Fun Mode" that tracks things your team actually cares about (but won't admit):

- 😂 **Joke Detector** — flags moments of actual humor
- 🎲 **Buzzword Bingo** — catches synergy, bandwidth, circle back, and your own custom watchlist
- 🔧 **Tool Complaints** — tallies every time someone blames Jira, Sentry, or the deploy pipeline
- 😤 **Boss Complaints** — diplomatic, obviously
- 🎭 **Most Dramatic Line** — the quote of the meeting
- 📊 **Confidence Score** — how energized does the team actually sound?

These aren't gimmicks. They surface real signal about team health, meeting culture, and morale — wrapped in something that makes people look forward to the recap instead of dreading it.

---

## Goals

1. Make standups **worth having** — actionable output, zero friction
2. Make the recap **worth reading** — structured, shareable, occasionally funny
3. Keep the tool **trustworthy** — your API key, your data, your browser
4. Stay **free forever** — you pay Anthropic for what you use (pennies per standup), nothing else

---

## How to use

1. Open [the app](https://assafbar2.github.io/standup-analyzer-but-for-free-with-surprise-goodies/) in **Chrome** (Web Speech API requirement)
2. Click **⚙ Settings** and paste your [Anthropic API key](https://console.anthropic.com/)
3. Click **⏺** to start recording
4. Talk. The transcript appears live. Analysis streams in the sidebar as you speak.
5. Click **⏹ Stop** when done — full analysis runs, results appear in tabs
6. Copy the Markdown summary and paste it wherever your team tracks things

---

## Privacy

- The transcript is sent to **Anthropic's API** for analysis (same as using Claude.ai)
- Your API key is stored in **your browser's localStorage only** — never transmitted anywhere else
- No analytics, no tracking, no backend, no database
- The source is 100% readable in your browser's DevTools

---

## Built with

- **Web Speech API** — browser-native transcription, no third-party STT service
- **Claude Sonnet** (via Anthropic API) — streaming JSON analysis
- Vanilla HTML, CSS, and JavaScript — no framework, no build step, no node_modules
