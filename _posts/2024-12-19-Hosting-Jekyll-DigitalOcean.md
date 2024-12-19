---
layout: post
title: "Hosting Jekyll Site on DigitalOcean"
date: 2024-12-19 12:54:36 +0000
categories: hosting jekyll ruby digitalocean
---

### Prerequisites:

- Domain (or Github Pages)
- DigitalOcean account
- Assumes your Jekyll project works locally
- Assumes you have pointers to digital ocean from your domain provider
- Assumes you have CNAME + A all setup for your custom domain

### Step 1

- After confirming your Jekyll project works
- Push up all the code to the git vc or your preferred vc software

### Step 2

- After logging in to DigitalOcean, create a new project in the left navbar, and follow the steps they require

### Step 3

- After project is setup, navigate to /manage/app_platform in the left navbar

### Step 4

- Press "Create App" in top right
- Connect your git vc or any other vc that is listed + repo
- then go through all req steps there

### Step 5

- go to the app you just created
- go to settings
- update domains with your www.[domain] or [domain]
- takes usually max of 5 minutes to see changes!

### Done!
