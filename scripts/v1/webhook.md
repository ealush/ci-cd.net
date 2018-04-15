---
title: webhook
description: Post (or Get) request to a webhook
toc: true
---

<img width="422" alt="Webhook notification example" src="https://user-images.githubusercontent.com/516342/37597214-66cdc4ec-2b87-11e8-94a9-0830dc222d1a.png">

> The webhook will execute a POST a JSON file to the specified address, or a GET request when no JSON file is found. It will use the shell to "process" the JSON file, so any environment variables included in the text will be transformed.

### Arguments
**No arguments** - Use environment variable `WEBHOOK` and `.webhook.json` file

| Argument | Role | Default
| --- | --- | ---
| 1 | webhook address | $WEBHOOK
| 2 | JSON to post | `.webhook.json`

> #### Example
> `curl ci-cd.net/v1/webhook | sh -s $MY_WEBHOOK ./.custom-webhook-message.json`

#### JSON Examples
CircleCI finished job -> Slack webhook
```json
{
  "attachments": [
    {
      "fallback": "$CIRCLE_PROJECT_REPONAME finished CI job",
      "color": "#27ae60",
      "author_name": "$CIRCLE_PROJECT_REPONAME",
      "author_link": "$CIRCLE_REPOSITORY_URL",
      "title": "CI workflow finished",
      "text": "Automated operation triggered by *$CIRCLE_USERNAME*",
      "mrkdwn_in": ["text"]
    }
  ],
  "channel": "#team-channel",
  "username": "CircleCI",
  "icon_emoji": ":robot_face:"
}
```