# signal-bot
A bot which sends notifications to a discord channel.
Used for trading signals, but can be adapted for other purposes.

## Setup
1. Fork the repository.
2. Setup a github action secret named `DISCORD_WEBHOOK_URL` with your discord webhook URL.
    - In a discord text channel, in which you want to receive notifications, go to the channel settings, then to "Integrations", and create a new webhook. Copy the webhook URL.
    - (You can find instructions on how to create a webhook [here](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).)
    - Now go to your forked repository, click on "Settings", then "Secrets and variables", then "Actions", and create a new "repository secret" with the name `DISCORD_WEBHOOK_URL` and the value being the copied webhook URL.
3. Now enable the github action in your forked repository.
    - Go to the "Actions" tab in your forked repository.
    - Click on "I understand my workflows, go ahead and enable them".

Now the bot should be running every night at 00:00 UTC and send notifications to your discord channel.

## Testing the setup
1. Delete the history file 'history_*.txt' if it exists (usually `history_150_200_15.txt`)
    - You can do this by clicking on the file in your repository and then clicking on the 3 dots in the top right corner of the file view and selecting "Delete file".
    - After that, select "Commit changes" in the top right corner and follow the instructions
2. Now go to the "Actions" tab in your forked repository and click on `Check indicators for SPYTIPS COOL STRATEGY` (below `All workflows` on the left).
3. Now select `Run workflow` and click on the green button (top right)
4. After one minute or so, the bot should have sent a message to your discord channel with the current indicators