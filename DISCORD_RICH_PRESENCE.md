# Set up Discord Rich Presence in Luma

Luma can optionally show a small activity on your Discord profile while you use it. This setup uses your own Discord application ID. Rich Presence is optional and can be turned off in Luma at any time.

## 1. Create a Discord application

1. Open the [Discord Developer Portal](https://discord.com/developers/applications) and sign in.
2. Select **New Application**.
3. Give it a name such as **Luma**, accept the displayed terms, and create it.
4. On the application's **General Information** page, copy the **Application ID**.

You only need the Application ID. Do **not** create a bot, copy a bot token, or share any secret. Luma does not need your Discord password or a bot token for Rich Presence.

## 2. Add the Luma image for Rich Presence

The Luma presence artwork is available as a standalone PNG in this repository: [Download Luma-Presence-Image.png](https://github.com/swibes/Luma/raw/refs/heads/main/Luma-Presence-Image.png).

1. Download the PNG using the link above.
2. In your Discord application, open **General Information** and upload that PNG as the **App Icon** (optional).
3. Open **Rich Presence → Art Assets**, upload the same PNG, and name the asset `luma` (lowercase).
4. The image is 1024 × 1024, suitable for Rich Presence art.

The code requests the exact asset key `luma`. If it is missing, Luma keeps a text-only activity instead of dropping the activity.

## 3. Enable it in Luma

1. Open the Discord desktop app and sign in to the account where you want the activity to appear.
2. Open Luma and go to **Settings**.
3. Find **Discord Rich Presence**, turn it on, and paste the Application ID you copied.
4. Save settings.

With the Discord presence fix applied, the activity includes a clickable **GitHub** button linking to [swibes/Luma](https://github.com/swibes/Luma). Discord does not show your own Rich Presence buttons to you, but other people viewing your profile can see them. The activity is generic and does not include media titles, links, or local file paths.

## 4. Choose who can see the activity

Discord controls whether your activity is shared. In Discord, open **User Settings → Activity Privacy** and enable **Share my activity** if you want other people to see it. Discord also lets you control sharing for individual servers. See [Discord's Activity Sharing FAQ](https://support.discord.com/hc/en-us/articles/7931156448919-Activity-Sharing-on-Discord-FAQ).

## If it does not appear

- Make sure the Discord **desktop app** is open and signed in. A browser tab alone may not provide the local Rich Presence connection.
- Double-check that you copied the **Application ID**, not an application secret or bot token.
- Confirm the toggle and ID are saved in Luma's settings.
- Check Discord's **Activity Privacy** settings and server-specific sharing controls.
- If the image is missing, confirm the Rich Presence Art Asset is named exactly `luma`.
- Restart Discord and Luma after changing the ID or art, then check your Discord profile again.

To stop sharing from Luma, turn off **Discord Rich Presence** in Luma's settings and save.
