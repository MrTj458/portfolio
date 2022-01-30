---
title: "Holowhoslive"
date: 2022-01-29T21:22:25-07:00
description: "A website that combines channels from both Youtube and Twitch. Centered around V-Tubers."
categories:
  - web-dev
github:
  - "https://github.com/MrTj458/HoloWhosLive"
coders:
  - MrTj458
image: "/img/holowhoslive.png"
tech:
  - name: Vue.js
    logo: "/img/vuejs.png"
    url: "https://vuejs.org/"
  - name: Python
    logo: "/img/python.png"
    url: "https://www.python.org/"
  - name: FastAPI
    logo: "/img/fastapi.png"
    url: "https://fastapi.tiangolo.com/"
  - name: PostgreSQL
    logo: "/img/postgresql.jpg"
    url: "https://www.postgresql.org/"
  - name: Redis
    logo: "/img/redis.png"
    url: "https://redis.io/"
  - name: Netlify
    logo: "/img/netlify.png"
    url: "https://www.netlify.com/"
  - name: Heroku
    logo: "/img/heroku.png"
    url: "https://www.heroku.com/"
  - name: Docker
    logo: "/img/docker.png"
    url: "https://www.docker.com/"
---

View this project live at https://www.holowhos.live/

_It may take a while to load since the API is on a free Heroku dyno. It will be significantly faster after the first load._

## First of all, What is a V-Tuber?

V-Tubers or "virtual YouTubers" are a form of live streaming where the streamer uses a virtual avatar, usually with a Japanese anime style, along with motion capture to create their own persona separate from their real selves. It really took off in 2020 when the whole world went on lock-down, and has continued to grow in popularity very quickly.

## Why did I make this site?

There are two main platforms where V-Tubers stream: Youtube and Twitch. I follow multiple of them on both platforms, so rather than switching between them to see who's live I combined them into one site.

## How does it work?

It uses both the Youtube and Twitch API's to find which channels are live and combines them in one place that links to their streams on the different services.

A PostgreSQL database is used to store the ID's of the different channels that should be on the website.

Due to the daily limits of the Youtube api the application uses Redis to cache the results from the API every 5 minutes, this way it won't go over and will keep working. The Twitch API doesn't have a daily limit like the Youtube API does, but it has a rate limit for rapid calls, so it caches Twitch data at the same time.

The site is hosted on two different platforms. The frontend is automatically build and deployed on Netlify. The backend is build
into a Docker image by a Github action and deployed to Heroku.
