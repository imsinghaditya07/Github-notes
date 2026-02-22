# 🔔 Managing GitHub Notifications (Inbox Zero)

> *As you start collaborating on more repositories or starring popular open-source projects, your GitHub notifications will quickly spiral out of control. It's time for to manage the noise.*

Developers often suffer from notification fatigue. If you get 50 emails a day from GitHub, you'll start ignoring all of them—meaning you might miss it when someone actually needs your review on a Pull Request.

---

## 🔕 1. The Problem: "Watching" vs "Participating"

Understanding why you are getting a notification is to fixing the problem.

*   **Participating:** You are receiving a notification because you opened an issue/PR, commented on it, or were specifically `@mentioned`. **These are high priority.**
*   **Watching:** You clicked the "Watch" button on a repository. You will receive notifications for **everything** that happens in that repo (every issue, every PR, every discussion). **This is usually a mistake.**

### Fix: Stop Watching Everything
1. Go to your github page and hit `Unwatch all` on repos you dont care.
2. If you only want to know about new releases (e.g., when React releases v19), change your repository watch settings from "All Activity" to **"Custom -> Releases"**.

---

## 📥 2. The GitHub Web Inbox

By default, GitHub sends you emails. **Turn them off.**

1. Go to **Settings** > **Notifications**.
2. Uncheck "Email" for basically everything, and ensure "Web and Mobile" is checked.
3. Access your notifications by clicking the **Inbox icon (the bell 🔔)** in the top right corner of GitHub (shortcut: press `g` then `n`).

Using the Web Inbox is far more powerful than email because of custom filters and quick actions.

---

## ✨ 3. The "Inbox Zero" Workflow

Treat your GitHub notifications like a to-do list, not a history log.

1. **Review:** Open the notification. (Hold `Ctrl` / `Cmd` and click to open in a new tab to keep your inbox open).
2. **Action:** Read the comment, merge the PR, reply, or simply acknowledge it.
3. **Done (Mark as Read):** Once you've handled it, click the **Checkmark (Mark as done)** in your inbox. This **removes** it from your inbox.

**The Goal:** By the end of the day, your GitHub Inbox should be completely empty.

If you read a notification but can't deal with it right now, **Save it for later** (click the bookmark icon). 

---

## 🗂️ 4. Custom Filters

If you are a maintainer or part of a large organization, you can create custom filters in the left sidebar of your Web Inbox.

For example, you can create a filter called `Needs My Review`:
```text
is:pr review-requested:@me
```
Or a filter for `Mentions`:
```text
mentions:@me
```

These act as smart folders, allowing you to prioritize being a code reviewer before looking at general chatter.

---

## 💡 Pro Tips

*   **Unsubscribe from dead threads:** If an issue you commented on 5 years ago suddenly gets revived and people are arguing, click "**Unsubscribe**" on the right sidebar of the issue immediately.
*   **GitHub Mobile App:** The GitHub mobile app has an incredible, swipe-based notification viewer (swipe to mark as done, save for later). It's the best way to clear out notifications while commuting.
*   **Action Required Checkbox:** In settings under Notifications, you can set it up so that failed CI/CD GitHub Actions send a push notification. Highly recommended so you know instantly if your build broke.
