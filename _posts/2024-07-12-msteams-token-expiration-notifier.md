---
layout: post
title: "MSTeams-Tickler: A CLI Tool for Microsoft Teams Token Expiration Notification"
description:
date: 2024-07-12 20:36:35 +0200
author: daniël 
image: '/images/msteams-hero.jpg'
tags: [cli, python, msteams, token, expiration, notification, macos]
tags_color: '#F08238'
---

## Introduction to MSTeams-Tickler for macOS 

MSTeams-Tickler is a simple tool that can save you a lot of time and cognitive strain. Moreover, it helps you stay
connected and prevents you from missing important notifications. It actively notifies you when your Teams token is
expired and requires a login.

### 1. Introduction of the Problem MSTeams-Tickler Solves

Many organizations require frequent login refreshes to maintain security. When a login token expires, Teams will display
a red bar at the top of the application, prompting the user to log in again. However, Teams doesn't actively notify users
when their token is expired. When your token expires, you will show up as offline and don’t get any incoming messages 
and calls. So the employer or colleagues can’t reach you and you might miss important events. In addition, it will look
like you are not working, which can give the impression that you are slacking. You can prevent this by checking Teams
frequently to see if a login is required. This is not a hobby of most people, and puts extra cognitive strain on your 
already overloaded brain. 

> What if there was a tool to actively notify you when your token is expired?

This is where MSTeams-Tickler comes in. You can set up a cronjob to run the check
every 15 minutes, and you will get a notification when the token is expired. The application uses the macOS notification
system to notify you when the token is expired.
To read more about MSTeams-Tickler and install it, see my GitHub profile [here](https://github.com/dan1elt0m/msteams-tickler)

### 2. Installation

`pipx install msteams-tickler`

### 2. Setup Cronjob 
```bash
crontab -e
```
In the crontab file, add the following line to run the check command at a regular interval:
```bash
*/15 * * * * mstc check
```

### 3. Conclusion
By two simple steps, you can prevent missing important notifications and stay connected with your colleagues. 
Happy coding!