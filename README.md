# Discord Bot

## Installation

```shell
git clone https://github.com/earth2travis/discord-bot.git
```

```shell
cd discord-bot
```

```shell
npm install
```

```shell
npm start
```

## Steps

- Create `.env` file in root
- Add DISCORDJS_BOT_TOKEN= to `.env`
- Create server on Discord (or add to existing server)
- Authorize bot on Server by replacing 1111 (with Client ID from application settings), visiting the URL: `https://discord.com/oauth2/authorize?client_id=1111&scope=bot` and selecting server from the drop-down menu.

## Permissions

- Server Settings > Roles > Add: Bots
- Make sure Bots is moved up in role hierarchy
- Give it General Permissions to Kick Members, Ban Members and Manage Roles

## Role Reactions

When users react to a message with certain emojis they are given roles.

1. Create Roles channel and Roles for JavaScript, CSS, HTML
2. Write message with the following text:
   - JavaScript - 🍑
   - CSS - 🍌
   - HTML - 🍎
3. Pin Message to channel
4. Replace ID of message to react to in `bot.js` for both `messageReactionAdd` and `messageReactionRemove`
5. Create roles and copy IDs to replace in switch statements for both `messageReactionAdd` and `messageReactionRemove`

## Webhooks

1. Go to channel you want to add the webhook to
2. Integrations > Webhooks > New Webhook > Name > Channel
3. Copy Webhook URL and paste into browser
4. Add WEBHOOK_ID= and WEBHOOK_TOKEN= with values in browser to `.env`

## Commands

- `$kick` 'ID'
- `$ban` 'ID'
- `$announce`

## Dependencies

- [discord.js](https://www.npmjs.com/package/discord.js) Node.js module that allows you to easily interact with the Discord API.
- [dotenv](https://www.npmjs.com/package/dotenv) Loads environment variables from a .env file into process.env.
- [nodemon](https://www.npmjs.com/package/nodemon) Automatically restarts the node application when file changes in the directory are detected.

## Resources

- Traversy Media [Create a Discord Bot With Node.js](https://www.youtube.com/watch?v=BmKXBVdEV0g)
