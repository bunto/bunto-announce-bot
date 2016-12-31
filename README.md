# Bunto Announce Bot

> Announce new releases & tags from Bunto repositories to Twitter: https://twitter.com/buntowaf.


## Deployment

* Create a twitter account
* Register a [new twitter oauth app](https://dev.twitter.com/docs/auth/tokens-devtwittercom)
* Set the permissions to `read/write`
* Generate a personal key for your account

Substituting for your new settings, run:

```
heroku login

heroku create your-new-announcer-bot

heroku config:set \
    BASIC_USERNAME="basic auth username" \
    BASIC_PASSWORD="basic auth password" \
    TWITTER_TOKEN="twitter oauth token" \
    TWITTER_TOKEN_SECRET="twitter oauth secret token" \
    TWITTER_CONSUMER_KEY="twitter consumer key" \
    TWITTER_CONSUMER_SECRET="twitter consumer secret"

git push heroku master
```

Register a new hook with your repo at `https://basic_username:basic_password@new-announcer.herokuapp.com`


## Development mode

Run locally:

```
heroku local web -p 4567
```


## What does it looks like?

Check out the [official Twitter account](https://twitter.com/buntowaf)
