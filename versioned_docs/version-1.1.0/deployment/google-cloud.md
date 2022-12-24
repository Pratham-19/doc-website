---
sidebar_position: 2
---

# Google Cloud Services

Following description guides for deployment of Telegram bot on Google App Engine.

## Prerequisites

- Google Cloud SDK
- Git
- Any text editor

## Steps to add bot to Google App Engine

1. Sign up or login in Google Cloud and create a new project.

2. Go through App Engine wizard.

3. Initialize Google Cloud SDK and go through the login process:

```
$ gcloud init
```

4. Clone your repo:

```
$ git clone https://github.com/{YOUR_REPO_NAME}.git
$ cd {YOUR_REPO_NAME}
```

5. Copy the API key of your bot.
6. Update config.ini at your repository folder - set TOKEN to the API key, HOOK_TOKEN to a random URL-friendly string, PROJECT_ID to Google Cloud project name.

7. Deploy the app:

```
$ gcloud app deploy
```

8. Open app in the browser to set a web hook: https://Google Cloud project ID.appspot.com/set_webhook. This should return:

```
{
"description": "Webhook was set",
"ok": true,
"result": true
}
```

9. Try to speak to your bot at https://t.me/{your_telegram_bot_id}!

:::info
For more info on how to configure your bot to communicate with Telegram, see [here](https://github.com/stop-cran/google-cloud-telegram-bot).
:::
