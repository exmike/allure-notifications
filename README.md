<h1>Allure notifications :sun_with_face:</h1>
<h6>for telegram, slack, skype, email, mattermost</h6>

<h3>Languages: :uk: :fr: :ru: :ukraine:</h3>

| Telegram | Slack |
:-------------------------:|:-------------------------:
![shakal_screenshot](readme_images/telegram-en.png) | ![shakal_screenshot](readme_images/slack-en.png)
| **Mattermost** | **Email** |
![shakal_screenshot](readme_images/mattermost-ru.png) | ![shakal_screenshot](readme_images/email_en.png)
| **Skype** | **Icq**  |
| Done | Wat? lol |


<h6>How to:</h6>

- [x] [Telegram config](https://github.com/qa-guru/allure-notifications/wiki/Telegram-configuration)
- [x] [Slack config](https://github.com/qa-guru/allure-notifications/wiki/Slack-configuration)
- [ ] [Email config](https://github.com/qa-guru/allure-notifications/wiki/Email-configuration)
- [x] [Skype config](https://github.com/qa-guru/allure-notifications/wiki/Skype-Bot-Configuration)
- [x] [Mattermost config](https://github.com/qa-guru/allure-notifications/wiki/Skype-configuration)


<h6>CommandLine options</h6>
All keys should be used with `-D`: <br/>

| key | description |
|:---:| :---------: |
| configFile | Path to JSON-config file |

```
java \
"-DconfigFile=${PATH_TO_FILE}" \
-jar allure-notifications-4.1.jar
```

If you want the project logo to appear in the upper left corner of the chart,
add the file logo.png to root of project


<h6>Config file structure</h6>
Here you can find config file structure for lib configuration.

```json
{
  "base": {
    "logo": "",
    "project": "",
    "environment": "",
    "comment": "",
    "reportLink": "",
    "language": "ru",
    "messenger": "telegram",
    "allureFolder": "",
    "enableChart": false
  },
  "telegram": {
    "token": "",
    "chat": "",
    "replyTo": ""
  },
  "slack": {
    "token": "",
    "chat": "",
    "replyTo": ""
  },
  "mattermost": {
    "url": "",
    "token": "",
    "chat": ""
  },
  "skype": {
    "appId": "",
    "appSecret": "",
    "serviceUrl": "",
    "conversationId": "",
    "botId": "",
    "botName": ""
  },
  "mail": {
    "host": "",
    "port": "",
    "username": "",
    "password": "",
    "enableSSL": false,
    "from": "",
    "recipient": ""
  },
  "proxy": {
    "host": "",
    "port": 0,
    "username": "",
    "password": ""
  }
}
```
You only need to fill needed options in `bot`, `base`, `mail` or `proxy` section. Please, be careful, `lang` and `messenger` fields are required!

If you want the project logo to appear in the upper left corner of the chart,
add file path to logo parameter in configuration

![](piechart.png)

Example for Telegram messenger:
```json
{
  "base": {
    "project": "some project",
    "environment": "some env",
    "comment": "some comment",
    "reportLink": "",
    "language": "en",
    "messenger": "telegram",
    "allureFolder": "build/allure-report/",
    "enableChart": true
  },
  "telegram": {
    "token": "asdhsdgfjsdfgFgjhg4831)@",
    "chat": "-1",
    "replyTo": ""
  }
}
```
