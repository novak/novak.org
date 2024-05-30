+++
title = "Contest Jockey"
slug = "contestjockey"
date = "2024-05-29"
author = "Michael Novak"
+++

{{< screenshot image="/images/contestjockey_screenshots.png" caption="Mobile and desktop Contest Jockey interface" >}}

Contest Jockey is a project I started with In The Money Media. We wanted to create a new contest platform for horse racing that was based on just a win wager, one horse per race. Traditionally most mythical money contests are based on a $2 Win/Place wager, but with Contest Jockey we decided to use the win wager but allow the player to choose any amount within their mythical bankroll to use. Each race within a contest has a minimum that must be played and those minimums can increase as the contest progresses. Allowing only one horse selection per race and it being based on a win gives players of all skill levels a chance to compete. You have to pick winners but you also have to manage your mythical bankroll as well.

I designed the branding, the interface and wrote all the code. This project was built using Typescript with a React frontend and a Node API project on the backend. There is a web based content management portal for administrators to manage each contest on the website. The infrastructure is hosted within a Kubernetes cluster using PostgreSQL as a database and Redis for caching.

This project is live at [https://contestjockey.com](https://contestjockey.com)
