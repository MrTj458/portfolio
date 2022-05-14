---
title: "Marked Notes"
date: 2022-05-14T16:27:57-06:00
description: "A website that allows you to write notes in Markdown and view them rendered as HTML."
categories:
  - web-dev
github:
  - "https://github.com/MrTj458/markednotes"
coders:
  - MrTj458
image: "/img/markednotes.png"
tech:
  - name: Vue.js
    logo: "/img/vuejs.png"
    url: "https://vuejs.org/"
  - name: Go
    logo: "/img/golang.png"
    url: "https://go.dev/"
  - name: Chi
    logo: "/img/chi.svg"
    url: "https://go-chi.io/"
  - name: PostgreSQL
    logo: "/img/postgresql.jpg"
    url: "https://www.postgresql.org/"
  - name: Heroku
    logo: "/img/heroku.png"
    url: "https://www.heroku.com/"
  - name: Docker
    logo: "/img/docker.png"
    url: "https://www.docker.com/"
---

View this project live at https://markednotes.herokuapp.com/

_It may take a while to load since the API is on a free Heroku dyno. It will be significantly faster after the first load._

## Why did I make this site?

I saw a couple of posts about applications for taking notes in markdown and being able to view them. I decided to make a web based version that I could use myself for free.

## How does it work?

It uses Go and Chi for the server storing the data in a Postgres database. The frontend is a Vue app made using Vite. The whole project is hosted on Heroku in a single Docker container.
