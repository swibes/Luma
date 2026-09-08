# Luma

A lightweight, customizable media downloader for Windows ♡

Made by [swibes](https://linktr.ee/swibes)

## Features

- Download video and audio from supported sites
- YouTube, TikTok, Instagram, X/Twitter, SoundCloud, and more
- MP3, WAV, OGG, and Opus audio
- Custom themes
- Download history
- YouTube Library support
- Automatic updates

## ♡ Connecting Your YouTube Account

Luma can connect to your YouTube account to display supported private library content, such as your **Liked Videos**.

Because Luma does not use a shared public Google OAuth client, each user needs to create their own Google OAuth credentials. This keeps your Google authorization separate from other Luma users.

### 1. Create a Google Cloud project

1. Go to the Google Cloud Console:
   https://console.cloud.google.com/

2. Sign in with your Google account.

3. Click the project selector at the top and choose **New Project**.

4. Name the project something like:
   `Luma`

5. Click **Create**.

---

### 2. Enable the YouTube Data API

1. Make sure your new Luma project is selected.

2. Open **APIs & Services → Library**.

3. Search for:
   `YouTube Data API v3`

4. Open it and click **Enable**.

You do **not** need to start a Google Cloud free trial or add a payment method for Luma's normal YouTube Library functionality.

---

### 3. Configure Google OAuth

1. Open **Google Auth Platform** for your project.

2. Configure the OAuth consent screen if Google asks you to.

3. Use:
   - **App name:** Luma
   - **Audience:** External
   - **Contact email:** Your Google email

4. While the app is in testing, go to **Audience → Test users**.

5. Add the Google account you want to use with Luma as a test user.

---

### 4. Create your OAuth client

1. Open **Google Auth Platform → Clients**.

2. Click **Create OAuth client**.

3. For **Application type**, choose:
   `Desktop app`

4. Name it:
   `Luma Desktop`

5. Click **Create**.

6. Click **Download JSON**.

⚠️ Keep this JSON file private. Do not upload it to GitHub, Discord, or anywhere public.

---

### 5. Connect it to Luma

1. Open **Luma**.

2. Go to **Settings → YouTube account**.

3. Click **Choose OAuth JSON...**

4. Select the JSON file you downloaded from Google.

5. Click **Save settings**.

6. Open **YouTube Library** and connect your account.

Your browser should open Google's authorization page.

---

### 6. Google may show an "unverified app" warning

If you created the OAuth app yourself and your project is still in testing, Google may display:

> Google hasn't verified this app

This is expected for your own testing OAuth project.

Make sure you're signing into the same Google account you added under **Test users**, then continue with the authorization.

Luma only requests the YouTube permissions needed for its library functionality.

---

### You're connected! ♡

After authorization, return to **YouTube Library** in Luma.

Your **Liked Videos** should now appear automatically.

You can select **Use this link** on a video to send its URL to Luma's downloader.

### About Watch Later

YouTube does not reliably expose the Watch Later playlist through the official YouTube Data API.

If Luma displays:

> Google didn't expose Watch Later for this account through the API

your account is still connected correctly. This is a YouTube API limitation and does not mean your Luma installation is broken.

---

### Disconnecting YouTube

To completely disconnect your account:

1. Remove Luma's access from your Google Account's **Linked apps** page.
2. Close Luma.
3. Press `Windows + R`.
4. Enter:
   `%LOCALAPPDATA%\Luma`
5. Delete only:
   `youtube_token.json`

Do not delete `settings.json` unless you also want to reset your Luma settings.

---

### Privacy

Your Google OAuth token is stored locally on your computer in:

`%LOCALAPPDATA%\Luma`

Your Google login is **not stored inside Luma.exe** and connecting your account does not modify the Luma executable.

Never share your OAuth JSON or `youtube_token.json` with anyone.
