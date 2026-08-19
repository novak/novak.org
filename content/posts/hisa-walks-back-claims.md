+++
authors = ["Michael Novak"]
title = "HISA Walks Back On What Happened"
date = "2026-08-19"
description = "Clarifying the most recent comments made by HISA"
tags = [
    "hisa"
]
categories = [
    "horse racing"
]
series = ["Horse Racing"]
+++

[Paulick Report: How He Did It](https://paulickreport.com/news/ray-s-paddock/how-he-did-it-marshall-gramms-actions-went-beyond-finding-a-security-flaw)
[HISA Original Statement](https://hisaus.org/news/hisa-charges-marshall-gramm-with-multiple-rule-violations-including-fraud-over-unauthorized-access-to-confidential-horse-health-information)
[Past the Wire](https://pastthewire.com/marshall-gramm-hisa-and-a-sport-wearing-blinkers/)
[In The Money Media](https://inthemoneypodcast.com/the-punishment-and-the-crime-inside-the-hisa-case-against-marshall-gramm/)

I am including the links above as I'll be citing quotations from them through this post to outline the stark differences in the two statements and how this corresponds to what actually happened.

### URL structure of the HISA Portal

Let's start with one of the most direct claims from HISA that came out after the supposed thorough investigation that left them with confidence in what happened.

> Lazarus said publicly that the idea this consisted simply of changing a horse number in a URL is “patently false,”

This is the original quote from HISA on what happened, while the quote below is the most recent statement from the organization.

> “What Dr. Gramm did after manually changing a URL once is what is at issue in this case and why HISA is pursuing charges against him,” Lazarus said in an additional statement provided Wednesday.

This is a direct contradiction to the earlier statement. How was HISA so confident in their report and understanding of what happened only to completely walk back their claims that the URL change was patently false? In a situation like this material facts are critically important. If you want to confidently control the narrative on a situation and claim others are completely lying you'd better be sure you have all your facts straight.

The script used to access the records did have what's called a 'loop' in computer software terms. The objective of this loop was to increment the number by one and request the next record. This is exactly what HISA attempted to claim was false. The script leveraged [Playwright](https://playwright.dev), which is a software framework that can open a browser window and issue commands to perform actions within that browser. This is a framework many website creators use to test that the functionality works as expected. It uses the browser just like any user would.

This is core to the argument here on the scope and complexity of what was done. You did not need to write code in order to view these records. Any owner or trainer that might be claiming a horse, or maybe buying from an online sale could pull up all these vet records whenever they needed to. The intent of accessing this information is exactly the same as Marshall's case. There needs to be separate discussions around utilizing the records for purposes within racing and the copying of records with computer software. Attempting to make this seem like a sophisticated attack on their systems completely misses the point. The HISA regulations the organization is claiming he violated had nothing to do with the code he wrote to pull down data. It had to do with the access to the information, which everyone had regardless of whether or not they wrote code to view the information.

### The system warned access was not authorized

> Lazarus also said the technology Gramm was using would have warned him multiple times that he wasn’t authorized to obtain the information.
>
> “He made the active choice to bypass those warnings,” she said.
> The records Gramm obtained didn’t come back in the same organized format a user would see when looking at an individual horse’s profile, Lazarus said. Instead, they came back as bulk data that had to be processed to be useful.

This statement is also something that did not come up during the initial press release or press conference. HISA makes no attempt at even specifying what "the technology" used is. Claude was not used to access the information, an AI agent did not go and pull all this information down for him. Claude was used to write code that would pull down this information. Once Claude had written the script to manage the browser session and open the URLs within the browser its job was done. From that point forward all that would have to be done was running the script to fetch data. 

### The HISA Portal Isn't Alcatraz

> She said HISA had tried to balance security with making the Portal easy enough for racing participants to use.
>
> “There was a decision to balance things out and to make it secure, but not … like Alcatraz because that would just make it impossible for us to have people use it,” Lazarus said.

I honestly don't even know where to start with this quote. HISA is claiming that this information is so sensitive and having access to it is such a significant problem, and yet they felt the need to "balance things out" so that it is usable. The problem with this statement is that restricting access to these records is fundamentally a basic problem. You show a user a page that says they are not authorized to access this record and that's it. How does this make the software impossible to use? 

You cannot in one breath scold someone for accessing the most sensitive information on a platform and then in the next breath say well, we didn't want to make it impossible to use so the records were just exposed to everyone. This is textbook gross negligence and if there's any claim that access to this information is in such violation of regulations then even HISA should be accountable for this as well. They had a responsibility to secure the information and they completely and utterly failed to do so, and by the statement above this sounds entirely intentional.

People like to use the analogy of a bank, well my bank website manages to make the software possible to use without compromising security. This claim implies that HISA intentionally made the product less secure, and they should have to answer to why.

### We may never know the extent of the access to records

> HISA eventually began tracking Gramm’s activity as investigators worked to determine what had happened, Lazarus said. According to Lazarus, Gramm stopped accessing the system after the past performances containing confidential veterinary information appeared on social media in June.

This statement appears to me as an admission that the system did not have sufficient logging in place prior to the leaked PPs. If they began to track his activity only after the leak, that means his access along with everyone else's prior to the leak would have been completely undetected. This is also troubling because HISA claims they are confident he was the only one accessing this information. If they do not have previous logs from the system how can they be sure of that? There could have been any number of owners or trainers that gained benefit from having access to the portal.

> HISA’s investigation included an independent forensic cybersecurity analysis by Arete, which, Lazarus said, found no evidence that anyone else had used the same method to improperly access confidential information.

This quote also does not make it clear to what extent there was even information to investigate. If basic logging did not exist in the platform, how were investigators going to find anything? This blanket statement has absolutely no value unless there is a clear papertrail that has been in place from the beginning. This is something HISA could very easily make public, which could help remove any doubt with their statements.
