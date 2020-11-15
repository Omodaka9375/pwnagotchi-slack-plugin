# pwnagotchi-slack-plugin
Let pwnagotchi post to your Slack!

![](gotchi.png?raw=true)

## The Slack Part
Make a Slack bot and add it your workplace as normal. Copy your **bot token**. Don't forget to add file upload and chat write permissions to the bot!

Instructions here: [Slack API token](https://slack.com/help/articles/215770388-Create-and-regenerate-API-tokens) 

## Pre-install
- Connect your pwnagotch in MANUAL mode
- SSH to your pi (eg. ssh pi@pwnagotchi.local)
- Type: sudo su (to swith to root)
- Type: pip3 install slackclient

To do it's job pwnagotchi needs three parameters "token", "channel" and "title". You can define these in config.toml at any time.

## Install the plugin
- Use SCP to browse your pwnagotchi via WinSCP or other client you prefer
- Navigate to /usr/local/share/pwnagotchi/availaible-plugins/ on your pwnagotchi
- Paste slack.py and slack.yml into this directory
- Navigate to /etc/pwnagotchi/config.toml and check if entries exist:
  - main.plugins.slack.enabled = true
  - main.plugins.slack.token = "YOUR-BOT-TOKEN-HERE"
  - main.plugins.slack.channel = "YOUR-CHANNEL"
  - main.plugins.slack.title = "POST-TITLE"

If not add the to the main.plugins.slack.* list and fill in the defaults.

## How to 
Every time you enter manual mode (eg. after a session) and have internet your pwnagotchi will post the report as PNG file, but only if new handshakes arived.

Enable the slack plugin from plugins page:
![](plugins.png?raw=true)

![](post.png?raw=true)

**Thats it, you are good to go!**
