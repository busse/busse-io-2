---
title: REST Fest 2016 Notes
seq: 160915
category: Events
---

## General Reference

* [REST Fest 2016 Wiki](https://github.com/RESTFest/2016-Greenville/wiki)
* [#restfest on Twitter](https://twitter.com/search?f=tweets&vertical=default&q=%23restfest&src=typd)
* [Livestream on Ustream](http://www.ustream.tv/channel/parismtscout?utm_campaign=t.co&utm_source=ustre.am%2FsjxS&utm_medium=social&utm_content=20160915134252)

*These notes are based on my personal experience at REST Fest 2016 and not intended to be comprehensive coverage of the event - YMMV.*

I left Richmond, VA at 6am Tuesday morning with my colleague Mark from our company [APIvista](http://apivista.com). We drove to Charlotte for a few meetings and left there Wednesday afternoon for Greenville, SC where REST Fest 2016 was held...

## Day 1: Hack Day

* [Hack Day Pitches](https://github.com/RESTFest/2016-Greenville/wiki/HackDay) presented by their proposers
* Chatted w/ [Brandee Shin](https://twitter.com/Brandee_Shin) about Gamified API Design / Teaching

> <a data-flickr-embed="true"  href="https://www.flickr.com/photos/bussefoto/29586939712/in/album-72157670599422244/" title="Stickies on the wall 01"><img src="https://c1.staticflickr.com/9/8551/29586939712_2f161fa296.jpg" width="500" height="375" alt="Stickies on the wall 01"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* After iterating on the idea a bit, we decided to try to deconstruct a variant of the classic [Lemonade Stand](https://en.wikipedia.org/wiki/Lemonade_Stand) game into an API discovery game.

> <a data-flickr-embed="true"  href="https://www.flickr.com/photos/bussefoto/29666636046/" title="Our game design in progress for #hack day - designing an #API for the Lemonade Stand game with Brandee Shin"><img src="https://c7.staticflickr.com/9/8574/29666636046_5d0f2abaa9.jpg" width="500" height="375" alt="Our game design in progress for #hack day - designing an #API for the Lemonade Stand game with Brandee Shin"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

> <blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">MVP complete: what a turn looks like. Building a game that teaches you REST API design w/ <a href="https://twitter.com/busse">@busse</a> <a href="https://twitter.com/hashtag/restfest?src=hash">#restfest</a> <a href="https://t.co/KqnGy2WHOm">pic.twitter.com/KqnGy2WHOm</a></p>&mdash; Brandee Shin (@Brandee_Shin) <a href="https://twitter.com/Brandee_Shin/status/776495595808776192">September 15, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

* We realized that there are at least three kinds of ways this could manfiest iteself beyond MVP, each with a different teaching objective:

  1. Just the act of trying to deconstruct the business log of the game and the relationship between the in-game entities into an API spec is something that could serve value for facilitating an API design training session

  2. The original idea we had was that there is an implicit set of rules behind an undocumented API that could be discovered through analog game play (e.g. cards & turns, with some randomization) appears to be viable with more iteration

  3. Building a working API service that simulates the Lemonade Stand game would be an excellent way to present a programming exercise for API consumption - build the services, with some behind the scenes logic and publish a spec with documentation - people could then compete to build the best script to automatically run the Lemondade Stand.

> <blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Hack day stand ups start at <a href="https://twitter.com/restfest">@restfest</a> with <a href="https://twitter.com/Brandee_Shin">@Brandee_Shin</a> (and <a href="https://twitter.com/busse">@busse</a> who is hiding) <a href="https://t.co/vd8zvqm5jd">pic.twitter.com/vd8zvqm5jd</a></p>&mdash; API Handyman (@apihandyman) <a href="https://twitter.com/apihandyman/status/776516407920033796">September 15, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

### Thoughts at the end of Day 1

* I really like the format of doing a Hack Day as the first day of a conference. It made for a great mixer and got people collaborating and working together right away.

* Very cool that they are [livestreaming the event](http://www.ustream.tv/channel/parismtscout?utm_campaign=t.co&utm_source=ustre.am%2FsjxS&utm_medium=social&utm_content=20160915134252) for those who can't make it!

* The content is very technical - much of what was hacked on and presented today was building on existing work - iterating on things to improve them - a great example of a community creating things together.

* [Awesome sponsor support](https://2016.restfest.org/us/sponsors.html) that provided resources to help make the conference a great experience.

## Day 2: Stack Day & Keynote

This day was a more structured series of talks - [the entire agenda is here](https://github.com/RESTFest/2016-Greenville/wiki/Agenda#friday-stackday--keynote). The main theme of the talks were the "stacks" that people use, "[StackDay is a chance for everyone to show off their favorite tools, libraries, tips and tricks](https://github.com/RESTFest/2016-Greenville/wiki/StackDay)."

* I gave the 3rd talk of the day, a somewhat ad-hoc presentation on [reverse-engineering 3rd-party APIs with mitmproxy/burp](https://github.com/RESTFest/2016-Greenville/wiki/Chris-Busse#using-mitmproxy--burp-for-reverse-engineering-undocumented-apis).

* It would have gone better if I could have gotten Reflector running so that my iPhone display showed next to the proxy intercept output ... next time...

* `placeholder for video of my talk after it is posted online`

* Here's a collection of Tweets during my talk:

> <div class="storify"><iframe src="//storify.com/chrisbusse/reverse-engineering-3rd-party-apis-with-mitmproxy-/embed?header=false&border=false" width="100%" height="750" frameborder="no" allowtransparency="true"></iframe><script src="//storify.com/chrisbusse/reverse-engineering-3rd-party-apis-with-mitmproxy-.js?header=false&border=false"></script><noscript>[<a href="//storify.com/chrisbusse/reverse-engineering-3rd-party-apis-with-mitmproxy-" target="_blank">View the story "Reverse Engineering 3rd-party APIs with mitmproxy/burp" on Storify</a>]</noscript></div>

* I was too busy prepping my talk during to really catch the first two. Of the afternoon ones, these are things I want to follow up on or look into deeper:

  * [Roman Hotsiy - ReDoc + generator-openapi-repo: API portal on GitHub in less than 10 minutes](https://github.com/RESTFest/2016-Greenville/wiki/Roman-Hotsiy#redoc--generator-openapi-repo-api-portal-on-github-in-less-than-10-minutes)
  * [Peter Rdogers (pjr) - Why JSON APIs Suck](https://github.com/RESTFest/2016-Greenville/wiki/pjr#why-json-apis-suck) (the 1060 / language / physics one)
  * [Jerome Louvel - Restlet Framework - NG](https://github.com/RESTFest/2016-Greenville/wiki/Jerome-Louvel#restlet-framework-ng)
  * (Microservices - Ronnie)
  * (Luke Stokes - Steemit.com) - the UI seems disingenous to show $ values - Goldberg asked a question about private messages / encryption [is there a way to use this with something like keybase?]
  * Dave Goldberg - his talk mentioned "The Nature of the Firm" book
    * "Technology Immensely Increases Intra-firm Efficiency"
    * "Web APIs Immensely Increase Inter-Firm Efficiency"
  * ChrisWhiteHQ - contact about movie idea - 500 words

## Day 3: 5in5 & Feature Talks

* Rob Zazueta - The Five API Monetization Models
  * "The success of an API program is measured by how well it moves a business toward its goals" - the only measure

  > <a data-flickr-embed="true"  href="https://www.flickr.com/photos/bussefoto/29112173674/in/dateposted-public/" title="Rob Zazueta - The Five API Monetization Models"><img src="https://c3.staticflickr.com/9/8481/29112173674_fa4f8acc5a.jpg" width="500" height="333" alt="Rob Zazueta - The Five API Monetization Models"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

  * 5 Monetization Models:
    1. Direct Monetization: ARPU = Total Revenue / Number of Users
    2. Use API Access as an Upsell Opportunity: e.g. Salesforce
    3. Driving Revenue Generating Activities Through Your API: Revenue recognition might happen downstream of the API call, but the API call was a necessary precendent. E.g. email send, affiliate links
      * Properly attribute the revenue generating activities to the apps that drove them using API keys
      * Follow the complete chain of application usage - many apps mak lead to a single revenue recognition
      * Not all calls durectly lead to revenue - measure **ARPU** against API usage
    4. Generating Revenue and Increase Distribution Through Strategic Partners / Affiliates
      * Carefully plan w/ your partners how success will be measured
      * For affiliates - pay only for directly-related revenue activities
      * Measure new customers brought in through partners / affiliates
      * Measure the **ARPU** of new customers brought in through partners/affiliates vs. ARPU of other custmers and total ARPU -- cohort analysus
    5. Improve Operational Efficiency and Decrease Time to Market for Internal Projects: this is where he is seeing the most movement these days - people turning to web services to do what SOA promised
      * **Comcast:** "Comcast went from about four weeks' lead tmie to just a few hours to onboard partners." - *Hain Thai, Senior Engineer, Comcast*
      * Review old project plans - measure avg time from inception to completion
      * Review existing provisioning proccesses. Measure the amount of employee time and actual time taken to completion
      * Seek new ways to decrease these numbers not only through APIs, but through other efficient processes
      * "Internal developer is just as important - anything you do for your external API portal you should do for your own developers"

* Leonard Richardson (New York Public Library) - The Magic Arrow

  > <a data-flickr-embed="true"  href="https://www.flickr.com/photos/bussefoto/29704886406/in/dateposted-public/" title="Leonard Richardson presents his talk The Magic Arrow at REST Fest 2016"><img src="https://c7.staticflickr.com/9/8282/29704886406_c18b806c00.jpg" width="500" height="375" alt="Leonard Richardson presents his talk The Magic Arrow at REST Fest 2016"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

  * Doing data architecture deisgn, **OPDS** was a magic arrow on his diagram
  * In Fielding's REST thesis, **HTTP** is the magic arrrow
  * Open Ebooks: a national collection for children who attend a Title I school or qualify for free/reduced-price lunch
  * Building an Ecosystem
    * Internet Archive
    * unglue.it
    * Standard Ebooks
    * Scandanavian bookstores
  * The alternative to SIP (3M) is The Sierra REST API - the branding of "Sierra" (an ILS) in it is problematic to be used with other ILS systems
  * ...but all the other ILS' support SIP
  * SIP is Extensible (Fielding 2.3.4.2)
  * 3M has friendly TOS for people wanting to extend SIP (Fielding 2.3.4.5)
  * These two properties make SIP a Magic Arrow
  * When an API is an arrow
    * What components can speak that protocol?
    * What components can consume it?
    * (left / right sides)
  * Lessons
    * Arrows (protocols) are more importand than boxes (APIs)
    * Good architecture can compensate for bad design
    * Extensibility and reusability need to be in the spec!
    * One API for ever product *category*, not every product
  
### The 5n5 talks begin... (some random notes)

* [apistylebook.com](apistylebook.com)
* [apis.guru](apis.guru)
* "For an industry that wants to do APIs on the scale of decades, we are a very trend-based group of people" - *[Erlend Hamnaberg](https://github.com/RESTFest/2016-Greenville/wiki/hamnis)*
* Mark gave his talk on the evolution of hosting - what was interesting is not the last 10 years, but the 10 years before
  * Be API First + Be Elegant In What You Do
* Irakli - Microservices & Culture
  * Culture is extremely important in microservices
  * "A team should should a product over its full lifetime" - *Lewis, Fowler* -- own the microservice from inception to deployment
  * The problem is that "Owner" != a guard :: Owner should be inception thru production, not in the sense that they're the only ones that can change the code
  * "Coordination" is a toxic word for Microservices - something we're trying to fix
  * A microservice should be small and simple enough that anybody in the organization can modify or rewrite it.

\###






