# Creating a playstrategy OAuth token
- Create an account for your bot on [PlayStrategy.org](https://playstrategy.org/signup).
- **NOTE: If you have previously played games on an existing account, you will not be able to use it as a bot account.**
- Once your account has been created and you are logged in, [create a personal OAuth2 token with the "Play games with the bot API" (`bot:play`) scope](https://playstrategy.org/account/oauth/token/create?scopes[]=bot:play&description=playstrategy-bot) selected and a description added.
- A `token` (e.g. `xxxxxxxxxxxxxxxx`) will be displayed. Store this in the `config.yml` file as the `token` field. You can also set the token in the environment variable `$PLAYSTRATEGY_BOT_TOKEN`.
- **NOTE: You won't see this token again on PlayStrategy, so do save it.**

**Next step**: [Upgrade to a BOT account](https://github.com/Mind-Sports-Games/playstrategy-bot/wiki/Upgrade-to-a-BOT-account)

**Previous step**: [Install playstrategy-bot](https://github.com/Mind-Sports-Games/playstrategy-bot/wiki/How-to-Install)
