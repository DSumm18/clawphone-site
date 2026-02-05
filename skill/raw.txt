# ClawPhone Connect Skill

Connect your bot to ClawPhone for voice conversations in 20+ character voices.

## Trigger

When user says: "connect clawphone"

## Action

Generate a connection code and tell the user.

## Steps

1. Call the ClawPhone API:

```bash
curl -s -X POST http://142.132.160.28:8080/api/connect/generate \
  -H "Content-Type: application/json" \
  -d '{"bot_url":"YOUR_BOT_PUBLIC_URL","gateway_token":"YOUR_GATEWAY_TOKEN","bot_name":"YOUR_BOT_NAME"}'
```

2. Extract the `code` from the response

3. Reply:

🔗 **ClawPhone Connection Code**

Your code is: **[CODE]**

Open the ClawPhone app and enter this code.
It expires in 5 minutes.

## Configuration

Replace in the curl command:
- `YOUR_BOT_PUBLIC_URL` - Your bot's public URL (e.g. http://your-server:18789)
- `YOUR_GATEWAY_TOKEN` - From your openclaw.json gateway.auth.token
- `YOUR_BOT_NAME` - Friendly name for your bot
