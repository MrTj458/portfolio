---
title: "Dgscorecard"
date: 2022-01-29T21:04:14-07:00
description: "A disc golf scorecard web app."
coders:
  - "MrTj458"
github:
  - "https://github.com/MrTj458/scorecard"
image: "/img/dgscorecard.png"
tech:
  - name: React.js
    logo: "/img/reactjs.jpg"
    url: "https://reactjs.org/"
  - name: TailwindCSS
    logo: "/img/tailwindcss.png"
    url: "https://tailwindcss.com/"
  - name: Go
    logo: "/img/golang.png"
    url: "https://go.dev/"
  - name: Chi
    logo: "/img/chi.svg"
    url: "https://go-chi.io/"
  - name: MongoDB
    logo: "/img/mongodb.jpg"
    url: "https://www.mongodb.com/"
  - name: Docker
    logo: "/img/docker.png"
    url: "https://www.docker.com/"

categories:
  - "web-dev"
---

## What does it do?

This site allows you to create scorecards to track scores during a round of disc golf. You can connect up to four accounts
into one scorecard and all the players will be able to view their scores.

It also has a 'bag' section that allows you to add the discs you have to help keep track of all of them.

## Why did I make this site?

I am a huge fan of disc golf and play all the time. I wanted to make my own version of [UDisc](https://udisc.com/), but
I wanted it to be entirely web based so it will run on any device as long as it can access the
internet rather than being a native mobile app. However, it is primarily styled to be used on a mobile device,
that way it can be used easily while out at the course.

## How does it work?

This site used Go with the Chi router as the server along with MongoDB as the database.
It creates a JSON API that the React.js frontend interacts with. It uses Docker to build out the individual components and combine
them into a single docker image that runs the entire application. This way I can host the entire site in one place
with a single image and not have to deal with separate font and back-end services like on my Holo Who's Live website.
