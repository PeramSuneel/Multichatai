# Multi-AI Chat Workspace

A lightweight, single-page workspace for preparing one prompt for ChatGPT, Claude, Gemini and Grok.

## What this website does

- Provides four provider panels in one responsive workspace.
- Lets you enter one common prompt and place it into each provider panel.
- Provides direct links to the official ChatGPT, Claude, Gemini and Grok websites.
- Provides one-click prompt copying for the three external website panels.
- Supports a genuine Gemini API conversation in the Gemini panel when you supply a Google AI Studio API key.
- Supports independent Gemini follow-ups, clear-all, dark/light themes and temporary in-page conversations.
- Does not save chat history or API keys to browser storage or a database.

## Important provider limitation

This is a static GitHub Pages website. A normal website cannot take over your signed-in sessions on ChatGPT, Claude or Grok or read their private replies. Therefore those three panels open the official provider websites and let you copy the prompt. Their responses and follow-ups take place on those provider websites, not inside this dashboard.

Gemini can be called directly through Google's official Gemini API, subject to the free tier and its current quotas. This is a real API integration, not a simulated response. The app does not send API requests to OpenAI, Anthropic or xAI.

**The website does not currently provide four automatic in-dashboard responses.** Doing that through existing consumer website accounts would require a different supported architecture, such as a browser extension, and must be separately assessed against each provider's rules. No login, CAPTCHA, rate-limit, subscription or security restrictions are bypassed here.

## Gemini API setup (optional)

1. Open [Google AI Studio API keys](https://aistudio.google.com/app/apikey).
2. Create a key for a project eligible for the Gemini API Free tier.
3. Keep the project on the Free tier. Do not attach paid billing or upgrade it.
4. Open the website and expand **Gemini API connection**.
5. Enter the key and send a test prompt.

The current model configured in the app is `gemini-3.1-flash-lite`. Model access, pricing, free-tier eligibility and quotas can change. Check Google's [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing) and [model documentation](https://ai.google.dev/gemini-api/docs/models) before use. If the free quota is exhausted or the model is unavailable, the request may fail; the app does not intentionally switch to a paid tier.

## Privacy and cost

- No backend, chat database, analytics or permanent chat history is included.
- Gemini API key is held in JavaScript memory for the current page session only. Refreshing the page clears it.
- The key is sent directly from the browser to Google's Gemini API. Anyone using browser developer tools can inspect a key entered into a client-side website. Use only for personal testing; do not share a session while a key is entered.
- Google may process free-tier API content under its applicable terms. Avoid confidential or sensitive information.
- No paid API request is made by this app to ChatGPT, Claude or Grok.
- Strict ₹0 use depends on keeping the Gemini project on the Free tier and staying within Google's free quota. This is not a guarantee of unlimited or permanent free service.

## Publish with GitHub Pages

1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`, then save.
4. Open the Pages URL displayed in the same settings page.

The site is static and requires no server or paid hosting.
