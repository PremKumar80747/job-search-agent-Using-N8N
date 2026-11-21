# AI Job Search Agent (n8n + Gmail + Gemini + Telegram)

Daily automation that reads job-alert emails from Gmail, removes duplicates,
ranks jobs against my profile using Gemini AI, and sends the top 5 to Telegram.

## Stack
n8n · Gmail API · Google Gemini API · Telegram Bot API

## Workflow
Schedule → Config → Gmail → Filter  → Gemini Ranking → Top 5 → Telegram

## Setup
1. In n8n: Workflows → Import from File → `job-search-agent.n8n.json`
2. Add credentials: Gmail OAuth2, Gemini API key (Query Auth, name `key`), Telegram bot token
3. Edit the **Config** node with your profile and keywords
4. Set your Telegram chat ID in the last node
5. Test, then activate

## Notes
- Dedupe memory works only on active (production) runs.
