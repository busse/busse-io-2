---
title: Bread - Reverse Engineering the Panera Bread App API 
seq: 160902
category: APIs
---

I have an upcoming talk at the [API Strat 2016](http://apistrat.com/) conference titled _Reverse Engineering Undocumentated APIs using mitmproxy_. While this talk will cover mitmproxy and a number of other tools, as well as examples from popular apps such as Instagram, Snapchat, Robinhood, and Pokemon Go, I wanted to include some original research. Panera Bread seemed a logical choice because I could come up with a outcome for the project that was relevant to me.

_Goal: Develop a node.js script that will place my "usual lunch order" from Panera by executing a single command from the command line._

## Activity Log:

### 160902: First run to POC that Panera Bread app is viable for reverse engineering

- Made an initial dump with `Burp` (yeah, the talk is supposed to be about using mitmproxy but I wanted to use Burp today), just to check for certificate pinning & whatnot. :thumbsup: No cert pinning. Ordered a Frontega Chicken, no tomato, no onion, soft dinner roll, added soft drink.
- Made another dump with `mitmproxy` to compare outputs, for a possible visualiztion library I'm thinking about. `./mitmdump -w 160902-mitmdump-panera.txt "~d panerabread\.com"`
- Observed that there are a number of calls, the API is very chatty with regard to sending nutrition info along with menu info, and that there appear to be two API gateways / domains:
  - `mobapi.panerabread.com` using `Server: Restlet-Framework/2.2.1`
  - `services-mob.panerabread.com` using `Server: nginx/1.8.0`
- Used [Postman](https://www.getpostman.com/) to execute a few calls
  - `validateClient`: This tells the Panera Bread API what client you are using, and it tells you if it is valid
  - `is-slot-available`: This tells the Panera Bread API what time you'd like to pickup your order, and it replies back as to whether that slot is available and if not, when the next available slot is
- There is a header of `api_token` that appeared to hold the same value between sessions that were hours apart. Need to see if it changes between devices or is just hardcoded.

I stopped short of writing the `Postman` calls to create a new `cart` (order), as it seemed like bad form to do that if I wasn't sure how to destroy the `cart`. I'm going to make a My Panera account and see, via the app, if when I have an order associated with a login, can I go in and clear it. I'll then try to recreate that sequence with code. Additionally, having the order be under my login may facilitate pickup/delivery and payment method in an easier manner.

