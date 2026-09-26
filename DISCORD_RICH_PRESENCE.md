# Set up Discord Rich Presence in Luma

Luma can optionally show a small activity on your Discord profile while you use the app. This setup uses your own Discord application ID. Rich Presence is optional and can be turned off in Luma at any time.

## 1. Create a Discord application

1. Open the [Discord Developer Portal](https://discord.com/developers/applications) and sign in.
2. Select **New Application**.
3. Give it a name such as **Luma**, accept the displayed terms, and create it.
4. On the application's **General Information** page, copy the **Application ID**.

You only need the Application ID. Do **not** create a bot, copy a bot token, or share any secret. Luma does not need your Discord password or a bot token for Rich Presence.

## 2. Enable it in Luma

1. Open the Discord desktop app and sign in to the account where you want the activity to appear.
2. Open Luma and go to **Settings**.
3. Find **Discord Rich Presence**, turn it on, and paste the Application ID you copied.
4. Save settings.

Luma should connect while Discord is open. Its activity is generic and does not include the media title, link, or local file path.

## 3. Choose who can see the activity

Discord controls whether your activity is shared. In Discord, open **User Settings → Activity Privacy** and enable **Share my activity** if you want other people to see it. Discord also lets you control sharing for individual servers. See [Discord's Activity Sharing FAQ](https://support.discord.com/hc/en-us/articles/7931156448919-Activity-Sharing-on-Discord-FAQ).

## If it does not appear

- Make sure the Discord **desktop app** is open and signed in. A browser tab alone may not provide the local Rich Presence connection.
- Double-check that you copied the **Application ID**, not an application secret or bot token.
- Confirm the toggle and ID are saved in Luma's settings.
- Check Discord's **Activity Privacy** settings and server-specific sharing controls.
- Restart Discord and Luma after changing the ID, then check your Discord profile again.

To stop sharing from Luma, turn off **Discord Rich Presence** in Luma's settings and save.
