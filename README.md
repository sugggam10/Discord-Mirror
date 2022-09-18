# Discord Mirror
Copy messages from other servers to your server.
I take no responsibility for using this bot against discord tos.

## Dependencies
- [Node v16.17.0+](https://nodejs.org/en/download/)
- [discord.js 8.15.0+](https://discord.js.org/#/)
- [discord.js-selfbot-v13](https://www.npmjs.com/package/discord.js-selfbot-v13)

## How to run
Run `node discord_mirror.js` on your terminal.

## Config explanation

## Token
```yml
token: "<DISCORD_ACCOUNT_TOKEN>"
```
This is the token of the discord account which have access to the channels you want to read. Note that this should be the token of a real user and not of the one of a bot. Click [here](https://www.androidauthority.com/get-discord-token-3149920/) to learn how to discover the token for your account.

## Webhooks
```yml
"webhooks": [
  {
    "token": "<WEBHOOK_TOKEN>",
    "id": "<WEBHOOK_ID>"
  },
  ...
]
```
This is the list of [webhooks](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks) to which messages to be replicated will be sent. For example, you can create a webhook in your discord server, then add it to `config.json` and when a message is sent, it will be copied to your server via the webhook. To create a webhook in your discord server go to `Server Settings` -> `Integrations` -> `Webhooks`.\
\
The token and the id of your webhook are embedded in the webhook url, for example, in:
`https://discord.com/api/webhooks/123456789/abcdefghijklmnopqrst`\
`123456789` is the ID, and `abcdefghijklmnopqrst` is the token.

## Channel IDs
```yml
"channel_ids": [
  "<CHANNEL_ID_1>",
  "<CHANNEL_ID_2>",
  ...
]
```
This is the list of channel IDs where when a message is sent, it will be replicated to all webhooks. To find the ID of a channel, you need to enable "Developer Mode" in your discord account settings, then you can right click on a channel and copy its ID.