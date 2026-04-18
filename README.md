# Mini App (Click redirect)

Static Telegram Mini App that opens an external Click payment server.

## How it works

- User selects a plan (`1m` or `6m`).
- On click, app opens external URL from query parameter `paymentBase`.
- It appends:
  - `telegramUserId`
  - `username`
  - `plan`
  - `source=telegram-miniapp`
  - `lang`

## Example URL

Use miniapp URL like:

`https://your-miniapp-domain.tld/?paymentBase=https://pay.example.com/click/start`

## Local run

```bash
caddy run --config /Users/dmitriy/Projects/work/yoga/Caddyfile
```

Then open:

`http://localhost:8088/?paymentBase=https://pay.example.com/click/start`

For Telegram Mini App production use HTTPS public domain.
