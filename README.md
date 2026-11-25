# Multi-AI Chat Workspace

A temporary, single-page multi-agent chat dashboard. Under the strict ₹0 setting, only Gemini is enabled, using a model listed on Google's official Gemini API free tier. ChatGPT, Claude and Grok remain visibly inactive; the app never sends requests to them.

## Important cost and privacy notes

- Gemini API free-tier access is limited by Google's model availability, quotas and rate limits. Free access is not unlimited.
- Keep the Google AI Studio project on the **Free** tier and do not attach paid billing. If the free quota is exhausted, requests should fail rather than be moved to paid usage.
- The API key is entered by the user at runtime and kept only in JavaScript memory. It is not saved in localStorage, sessionStorage, cookies, or this repository. Refreshing the page clears it.
- This browser-only approach is intended for personal use. A key used in a browser can be inspected by the person using the browser and should not be shared. Do not publish or share a dashboard session while a key is entered.
- Google states that content from the free tier may be used to improve its products. Do not submit confidential or sensitive information unless comfortable with Google's applicable terms.
- No permanent chat database is used. Conversation context exists only in the open page.

## Get a Gemini API key

1. Open [Google AI Studio](https://aistudio.google.com/app/apikey).
2. Sign in with your Google account.
3. Create an API key in a project that is eligible for the Gemini API Free tier.
4. Confirm the project is not linked to paid billing. Do not upgrade it.
5. Open the deployed dashboard and paste the key into **Gemini connection**.
6. Send a test prompt.

Google's free-tier models, limits and availability can change. Check [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing) before use. The configured model is `gemini-3.1-flash-lite`; if Google retires or changes access to that model, update the model ID only after checking the official model list and free-tier pricing.

## Publish with GitHub Pages

1. Open this repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select branch **main** and folder **/(root)**.
5. Save and wait for GitHub Pages to publish.
6. Open the Pages URL shown in Settings → Pages.

The site is static, so no server or database is required for this first Gemini-only version.

## Current provider status

| Provider | Status under strict ₹0 mode |
|---|---|
| Gemini | Enabled, subject to Google's free-tier quota |
| ChatGPT / OpenAI API | Disabled; no ongoing free API allowance assumed |
| Claude / Anthropic API | Disabled; trial credits are not treated as an ongoing free tier |
| Grok / xAI API | Disabled; no ongoing free API allowance assumed |

The app does not substitute another provider's model while displaying a provider's brand.
