---
layout: default
title: Who should write the sample apps for an Enterprise API Product?
seq: 170303
category: uncategorized
---

> *Hey Busse! On an Developer Platform, where do you think the responsibility of providing sample apps for the API Consuming developer lies? Who creates, owns, and maintains it - the Engineering Team who owns the API Product, or the Developer Platform Team responsible for running the portal and the developer relations program?*

While not quite as common as the "how should we version our API?" question, this is something I'm seeing come up more as enterprises scale in to larger API programs with multiple delivery teams involved. They come to realize the amount of effort that goes in to raising something up as a truly "first class" API product, and questions come up as to "who owns what?"

In my opinion, sample apps illustrating API consumption are part of the overall "documentation" that should be provided when an API is published to an audience - especially a 3rd-party audience outside of the organization like strategic partners and public developers.

I find myself being able to make an argument for both approaches implied in the question above - that the API Product team should provide sample apps, or that some centralized Platform / Developer Relations Team should build sample apps.

## Sample apps as a deliverable from the API Product Engineering Team

I see at least three reasons why it would make sense for the API Product Engineering Team to create sample apps for their APIs:

  1. **Fundamentally, if your organziation is treating APIs as a real product, delivered by a product team, then the "supporting" assets such as documentation and sample apps are the responsibility of that product team.** If your Tech Writers are aligned with the product team, or whoever is writing the OpenAPI or similar specification in the first place is aligned with the team, then so should the efforts to create the sample app.

  2. **The Team is already intimately familiar with the implementation details of the API**, and can use the sample app to illustrate the business and technical use cases they've been asked to address. There's less of a chance of something getting "lost in translation" between two teams when the original intent of a newly built API is being published.

  3. **The Team is likely already working on related scope in the current sprint(s).** In other words, it is one less inter-team deliverable to have to coordinate in an enterprise software engineering organization. In my experience, this can save weeks (if not months) of time between when an API is published and when its sample app is published. This becomes even more evident when the API gets modified - you'll want to be able to ship an updated sample app in lockstep with publishing an updated API.


## Sample apps as a deliverable from a centralized Developer Platform / Relations Team

Again, thre's at least three reasons why it might make sense for the sample apps to be owned and delivered by a centralized team on the API program:

  1. The strongest argument I see for having the Developer Platform or Relations team - or really, any competent team other than the team that originially built the API - build the sample app, is that **it acts as an additional check on the quality of the API.** Having developers write an implementation against the API in a "safe" environment like this gives you the opportunity to surface issues before the API consuming teams (possibly external to your organization) do. It also give the chance to get improvements into the backlog of the API producing team in less time.

  2. **The sample app may need to orchestrate APIs from multiple teams.** In this case, having an independent team develop the sample app allows them to focus on that as a more complex task. They can learn how to use all the necessary APIs and put them together in one cohesive sample. Similar to #1 above, this approach gives them the opportunity to independently surface issues between the various APIs (maybe one API returns an `ID` as a `string` and the other as an `integer`...)

  3. **Ensuring consistency of sample apps across multiple API Products.** Just as one of the goals of good API Governance is to make it look like one cohesive entity is publishing a unified set of APIs, making the sample apps look cohesive is important too. Having one centralized team dedicated to that task can help ensure that outcome This is even more true if it's less likely that the sample apps have the same level of governance and up-front consistency checkes as the API specs.

## Conslusion

In the end, it comes down to the question: 

> *Where can we get the most value from our sample apps, and who is going to be able to bring them to market in a timely and accurate manner so that they act as an effective learning tool for the developers using our APIs?*

**The answer to that will vary from organization to organization, but in the end, the developers using the sample apps to better understand your APIs will appreciate your teams' efforts!**

---

*Questions or feedback on this article can be sent to <a href="mailto:chrisbusse@gmail.com">chrisbusse@gmail.com</a> or entered in the <a href="https://github.com/busse/busse-io/issues">Issues for the busse.io GitHub repo</a>. If you need help with your API Program, that's what we do at <a href="http://apivista.com">APIvista</a>.*

---

<p align="center">
If you :heart: this article, give it a Like, Retweet or Reply!

<blockquote class="twitter-tweet" data-lang="en" align="center"><p lang="en" dir="ltr">Who should write the sample apps for an Enterprise API Product? <a href="https://t.co/UljtPgB9p3">https://t.co/UljtPgB9p3</a> | <a href="https://twitter.com/hashtag/APIs?src=hash">#APIs</a> <a href="https://twitter.com/hashtag/devrel?src=hash">#devrel</a> <a href="https://twitter.com/hashtag/governance?src=hash">#governance</a></p>&mdash; Chris Busse (@busse) <a href="https://twitter.com/busse/status/837652745138102272">March 3, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
</p>