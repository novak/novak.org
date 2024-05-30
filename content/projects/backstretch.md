+++
title = "Backstretch"
slug = "backstretch"
date = "2024-05-29"
author = "Michael Novak"
+++

{{< screenshot image="/images/backstretch_screenshots.png" caption="Mobile and desktop interface for Backstretch" >}}

Backstretch is a web based management platform for horse racing stables. As an owner you can follow along with updates regarding your horses including entries, results, financials, and more. I designed the branding, interface and built all the code for the frontend and backend systems.

The frontend is a React web application, the backend is a node API project using a PostgreSQL database as well as Redis for caching and job processing. There are a few data processing applications in the backend that are written in Python. The frontend and backend API are written in Typescript. The infrastructure is hosted on a kubernetes cluster.

This is live on the web at [https://backstretch.app](https://backstretch.app)
