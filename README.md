![InspiroBot](http://i.imgur.com/uPh4T8d.png)
# InspiroBotSlack
Slack integration with InspiroBot.me

## How is this different than `bhberson/InspiroBotSlack`:
- There is shuffle capability before posting to a channel. Since there are NSFW images, it helps to verify before posting.
- This is maintained while the other isn't. I tried submitting PR's to improve the other project but the author did not respond.

## Local development
Use ngrok (https://api.slack.com/tutorials/tunneling-with-ngrok) to test commands locally.

## Slash Commands
This works in all channels, within Slack Integration Choose Slash Command and setup something similar to this:
![Create an App and enable slash command](https://i.imgur.com/aADWoQV.png?1)

Create a new slash command:
![Create a new Slash command](https://i.imgur.com/XpUqtBc.png?1)

To configure request URL (indicated as 1, in image below), you have the following options:
- Use my Heroku deployment with the following Request URL: `https://inspirome-slack.herokuapp.com/slash`
- Clone the repo yourself and upload the Node.js app to your own private webserver and configure like it is below:
![Image of Slash Command Settings](https://i.imgur.com/yMRLEbc.png)

Once added, when you call `/inspire`, you will be presented with following options visible only to yourself:
- *Send*, send the image shown to channel, so that its visible for everyone.
- *Reshuffle*, change the image from Inspirobot to something else, visible only to you.
- *Cancel*, cancel sending an image. The message will be deleted without sending anything.
![Once added you have the ability to shuffle](https://i.imgur.com/mVDAWef.png?1)

Once you hit Send, the posted message looks this way:
![Posted message](https://i.imgur.com/dr955Yw.png)

Image for icon: http://inspirobot.me/website/images/inspirobot-dark-green.png
