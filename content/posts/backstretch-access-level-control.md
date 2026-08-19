+++
authors = ["Michael Novak"]
title = "Access Level Control"
date = "2026-08-19"
description = "An example of building proper access level control for a stable management platform"
tags = [
    "hisa",
    "backstretch"
]
categories = [
    "horse racing"
]
series = ["Horse Racing"]
+++

In recent years I built a stable management platform for horse racing owners and trainers named Backstretch. The goal of this product was to provide a modern platform for managing a racing stable. This included the ability for owners and trainers to see updates on horses within their stable, store records around training, billing and even vet records as well. This platform had the ability to handling invoicing for trainers, allowing them to not only create invoices easily but accept payments right on the platform. 

Ultimately the platform did not gain the traction it needed and was significantly expensive to operate while not generating any revenue. The product is no longer available, but I do want to discuss how I implemented access control on the platform as it is very relevant to the current industry news. It is worth pointing out that this was a complete solo project and I was the only individual that did the user interface design, server side software and the website software. This product was optimized for a desktop as well as a mobile phone, making it easy for users to access their information on the go.

{{< screenshot image="/images/backstretch_blog_screenshot.png" caption="Mobile and desktop interface for Backstretch" >}}

### Technical Implementation

This section will get fairly technical but I will explain this in a way that non-technical readers can understand what the code is doing. For those with a technical background this should be straight forward to follow.

```typescript
const stableId = req.params.id != null ? parseInt(req.params.id) : -1;
const horseGuid = req.params.horseGuid;

if (stableId === -1 || horseGuid == null) {
  ErrorUtil.handleClientError(new Error('Stable or horse not found'), 404, res);
  return;
}

const account = await AccountModel.get(parseInt(req.headers.account as string));
if (account == null) {
  ErrorUtil.handleClientError(new Error('Account not found'), 404, res);
  return;
}

const stable = await StableModel.get(stableId, account.id);
if (stable == null) {
  ErrorUtil.handleClientError(new Error('Stable not found'), 404, res);
  return;
}
```

The code above is used any time data is requested from the server. The first thing this does is validate the incoming parameters. The account validation shown here is actually a second pass, there's an initial check not shown here that verifies the authentication token provided in the request. The code to get the stable passes the account id to ensure that the account making the request is a member of the stable the data is associated with. The `req.headers.account` is actually injected by the server after validating the authentication token. You cannot supply a user id in a request to mask another user, you need the authentication token that is received when you log into the web portal. 

This is itself a really simple implementation. What this does demonstrate is that you don't need a highly sophisticated system to provide the basics of user and data protection. The core of my argument in the HISA case is that this level of basic verification simply did not exist within their portal. 

## Responsibility of privacy and protection

With Backstretch my intent was to provide a secure and reliable platform to manage your stable. A platform such as this has access to highly sensitive information. This might be financials or even communications between owners and trainers that contain proprietary information. I felt and continue to feel that building a platform such as this comes with extreme ownership on the integrity of privacy and protection for all users of the platform. A data breach of any kind exposes direct risk to users of the platform. This is not something I have ever taken lightly in my career. Security is the most important aspect of any platform, but especially platforms that contain highly sensitive information on behalf of their users.

I am happy to share any additional details or discuss anything technical on this project or any other personal project I have worked on. It is important as an industry to hold ourselves to the highest of bars when it comes to building modern software platforms to advance horse racing for everyone.
