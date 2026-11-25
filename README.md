# Multi-AI Chat Workspace

A free, static, single-page workspace for preparing prompts for ChatGPT, Claude, Gemini and Grok through their official websites.

## Features

- Four dedicated provider panels.
- Enter one common prompt and distribute it into all four panels.
- Edit each provider's prompt independently.
- Copy each prompt with one click.
- Open ChatGPT, Claude, Gemini or Grok in its official website.
- Dark and light themes.
- Clear all prompt drafts.
- Responsive desktop and mobile layout.
- No API integrations, API keys, backend, database, or saved chat history.

## Important limitation

This project deliberately uses **no APIs**. It cannot automatically submit prompts to the providers, read their replies, or import their conversation histories. The user opens the official provider website, pastes the copied prompt, and continues the conversation there.

A normal static website cannot access private sessions or responses inside other websites. This workspace does not automate logins, bypass provider restrictions, or simulate AI responses.

## Privacy and cost

- The website does not make AI API requests.
- It does not ask for or store API keys.
- Prompt drafts exist only in the current page memory and are cleared when the page is refreshed or the Clear all button is used.
- No backend or paid hosting service is required; GitHub Pages can host the static files.
- The provider websites have their own accounts, privacy policies, and usage limits.

## Publish with GitHub Pages

1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`, then save.
4. Open the Pages URL displayed in the settings page.
