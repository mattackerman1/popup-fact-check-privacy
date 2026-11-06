# Privacy Policy — Pop-Up Fact Check

Effective date: November 5, 2026  
Product: Pop-Up Fact Check browser extension (Chrome / Firefox)  
Developer: Matthew Ackerman  
Contact: mattackerman80@gmail.com

## Summary
Pop-Up Fact Check does not operate a backend server and does not create an account with us. The extension runs in your browser, stores settings locally, reads YouTube captions for videos you open, and sends transcript excerpts and claims only to the AI provider(s) you configure with your own API key.

## Data the extension handles
1. **Settings you enter** — enabled/mode toggles, provider and model ids, optional second-opinion settings, web-search toggle, and API keys for OpenRouter, xAI, Anthropic, OpenAI, and/or Google Gemini. Stored in `chrome.storage.local` / `browser.storage.local` on your device.
2. **YouTube caption / timed-text content** for the active `youtube.com` video, plus video id and publish date when available — used to spot and check claims (or produce fun-fact cards).
3. **Cached fact-check cards** — stored locally so the same caption chunk is not re-queried every time. You can clear this cache from Options.

## What is sent where
- **To YouTube:** content scripts run only on `https://www.youtube.com/*`. The extension may refetch an allowed `https://www.youtube.com/api/timedtext` URL with your normal YouTube cookies (`credentials: "include"`) solely to obtain captions. Those cookies are not sent to AI providers.
- **To your chosen AI provider(s):** HTTPS requests with your API key (`credentials: "omit"`) containing system/user prompts, caption chunk text, and extracted claims. If you enable web search and the provider supports it, the provider may perform web search (and for xAI, X search) using claim-related queries. Source links shown on cards are URLs returned by that provider.
- **To the developer / Pop-Up Fact Check:** nothing. There is no Pop-Up Fact Check analytics, crash reporter, or account server in this extension.

## Sharing / selling
We do not sell your data. We do not share extension data with third parties except the providers you explicitly configure, under those providers’ own terms and privacy policies.

## Retention
Local settings and cache remain until you clear them, clear site/extension data, or uninstall. Provider retention is governed by the provider you use.

## Children’s privacy
The extension is not directed at children under 13.

## Your choices
- Do not enter an API key → the extension cannot check claims.
- Turn off “Run on YouTube” in Options.
- Disable web search in Options.
- Use “Clear cached verdicts”.
- Remove the extension to delete its local storage.

## Changes
If this policy changes, the effective date above will be updated on the hosted page.

## Contact
For support or privacy questions about Pop-Up Fact Check, email: mattackerman80@gmail.com
