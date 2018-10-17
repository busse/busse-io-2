---
title: Project Charter - Utility to Drive Review of My Pinboard.in'd Links
seq: 181017
category: Projects
---

As a user of the Pinboard.in link saving service, I want a simple utility that integrates with my GitHub Pages / Jekyll workflow to drive me to review the links on a regular basis and generate posts about those links.

MVP Acceptance Criteria:

  - The utility runs automatically in the background on a cadence I specify
  - The utility accesses Pinboard.in via its API
  - The utility outputs one draft blog post per cadence window (time since last run until the current run), containing all links, titles, and notes in Pinboard.in in a format that is read to edit
  
This project has been started at the GitHub repo: [busse/pinboard-jekyll-drafter](https://github.com/busse/pinboard-jekyll-drafter)