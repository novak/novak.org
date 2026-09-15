+++
title = "Backstretch"
slug = "backstretch"
date = "2024-05-29"
author = "Michael Novak"
+++

{{< screenshot image="/images/backstretch_screenshots.png" caption="Mobile and desktop interface for Backstretch" >}}

Backstretch was a web based management platform for horse racing stables. As an owner you could follow along with updates regarding your horses including entries, results, financials, and more. I designed the branding, interface and built all the code for the frontend and backend systems.

The frontend was a React web application, the backend was a node API project using a PostgreSQL database as well as Redis for caching and job processing. There were a few data processing applications in the backend that were written in Python. The frontend and backend API were written in Typescript. The infrastructure was hosted on a kubernetes cluster.

Backstretch has since been sunset. The platform did not gain the traction it needed to cover its operating costs. You can read more about how it was built in [Access Level Control](/posts/backstretch-access-level-control/).
