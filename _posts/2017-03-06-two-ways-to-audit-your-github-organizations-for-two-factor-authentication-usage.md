---
title: Two ways to audit your GitHub Organizations for Two-Factor Authentication usage
seq: 170306
category: uncategorized
---

On a call with a client, one of the Tech Leads implored everyone to make sure they had Two-Factor Authentication (2FA) set on their GitHub accounts.

**The request got me a bit philosophical:** I theorize that GitHub, as a platform, has more people using "personal accounts" in a "professional context" than many other platforms. In other words, while almost everyone has a "work email", I think it is may somewhat common for GitHub users to just have one account that they use for all repos - work and personal (community / hobby).

This creates a scenario where there may be less and/or more relaxed administrative oversight. Policy is helpful, but verification is necessary.

> *The new GitHub Business plan may help this for some enterprises, with its introduction of [SAML/Single Sign On](https://help.github.com/articles/managing-member-identity-and-access-in-your-organization-with-saml-single-sign-on/) - but that isn't for everyone, so...*

There are two ways to audit the use of 2FA on GitHub: Through the UI, and through the API (as it should be!)

## Verifying 2FA usage by GitHub Organization Members using the UI

[This is pretty simple](https://help.github.com/articles/viewing-whether-users-in-your-organization-have-2fa-enabled/). Navigate to any Organization you're an Owner of, then click the `People` tab. There will be a dropdown menu labelled `2FA` - select `Disabled` to see who in the Organization isn't using 2FA.

<img src="/assets/170306-2FA-admin-screen.png" width="100%">

## Verifying 2FA usage by GitHub Organization Members using the API

Also, pretty simple, but it does require you to have a personal API token. After you've [generated a token](https://github.com/blog/1509-personal-api-tokens), you run:

    curl -H "Authorization: token [yours]" "https://api.github.com/orgs/[orgname]/members?filter=2fa_disabled"

You'll then get back a nice JSON response that shows who does not have 2FA enabled:

```javascript
[
  {
    "login": "username",
    "id": 1234567,
    "avatar_url": "https://avatars1.githubusercontent.com/u/1234567?v=3",
    "gravatar_id": "",
    "url": "https://api.github.com/users/username",
    "html_url": "https://github.com/username",
    "followers_url": "https://api.github.com/users/username/followers",
    "following_url": "https://api.github.com/users/username/following{/other_user}",
    "gists_url": "https://api.github.com/users/username/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/username/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/username/subscriptions",
    "organizations_url": "https://api.github.com/users/username/orgs",
    "repos_url": "https://api.github.com/users/username/repos",
    "events_url": "https://api.github.com/users/username/events{/privacy}",
    "received_events_url": "https://api.github.com/users/username/received_events",
    "type": "User",
    "site_admin": false
  }
]
```

The advantage of this method is that you can script the audits to run at a regular interval. (Maybe even pipe the output to Slack...) For organizations that use contractors, have "turnover" in their GitHub Orgs, or are enterprises that allow users to use "personal" GitHub accounts on their Organizations, this could be a useful approach to keeping up good 2FA hygene.

## Not getting compliance? Kick 'em out!

GitHub also had a feature, [that enables an Organziation owner to remove everyone from an Organization who isn't using 2FA](https://help.github.com/articles/requiring-two-factor-authentication-in-your-organization/). While that might be a bit extreme, if it's something that's important to you and after several prompts people aren't complying, it might be a useful option.

---

*Questions or feedback on this article can be sent to <a href="mailto:chrisbusse@gmail.com">chrisbusse@gmail.com</a> or entered in the <a href="https://github.com/busse/busse-io/issues">Issues for the busse.io GitHub repo</a>. If you need help with your API Program, that's what we do at <a href="http://apivista.com">APIvista</a>.*

---

<p align="center">
If you :heart: this article, give it a Like, Retweet or Reply!

<blockquote class="twitter-tweet" data-lang="en" align="center"><p lang="en" dir="ltr">Two ways to audit your GitHub Organizations for Two-Factor Authentication usage <a href="https://t.co/zcaJgw1XsL">https://t.co/zcaJgw1XsL</a> <a href="https://twitter.com/hashtag/Security?src=hash">#Security</a> <a href="https://twitter.com/hashtag/github?src=hash">#github</a></p>&mdash; Chris Busse (@busse) <a href="https://twitter.com/busse/status/838827485080997888">March 6, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
</p>
