---
title: "Resurrecting fineants"
date: 2018-06-08T21:51:11+10:00
summary: "I decided to resurrect a 4 years old app. These are the tradeoffs I made to ship an update as soon as I could, and why that's valuable."
---

I recently submitted the first update in 3.5 years of [fineants](https://itunes.apple.com/au/app/fineants-saving-goals-tracker/id888444078?mt=8) for review to the App Store.

![Screenshot of fineants 1.3.0 on the App Store](https://s3.amazonaws.com/assets.shipping.software/fineants-1.3.0.png)

The app helps visualise delayed gratification to reach your saving goals. A big part of saving money is not spending them. Users can log the things they don't buy on fineants, keeping track of how much money they have been saving.

I decided to start working on fineants again after such a long time because I noticed a small but steady stream of users and In-App Purchase upgrades.

![fineants's lifetime sales as of June 2018](https://s3.amazonaws.com/assets.shipping.software/fineants-lifetime-sales-2014-to-2018.png)

_I wish I knew what caused that spike around October 2017._

I asked myself, how far can I take this?

I learnt a lot since the last update to the app. I've also become very **opinionated**. This could be a fun way to apply some of those theories on how to execute on software products.

One such opinion is the importance of the **feedback loop**. The faster you can get software in the users' hands the more you can learn. The more your learn the better your products get.

I bumped into this tweet from [Baremetrics](https://baremetrics.com/)' founder [Josh Pigford](https://twitter.com/Shpigford/):

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">22/ You will never attain the perfect product. The effort required to “polish” a product has diminishing returns. Yes, the details matter. But “shipped” is better than “perfect”. Startup graveyards are littered with companies who never actually launched anything at all.</p>&mdash; Josh Pigford (@Shpigford) <a href="https://twitter.com/Shpigford/status/1001840358626660352?ref_src=twsrc%5Etfw">May 30, 2018</a></blockquote>

<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

It resonates a lot with me. Along the same lines is [Kent Beck](https://twitter.com/KentBeck) [quote](http://wiki.c2.com/?MakeItWorkMakeItRightMakeItFast):

> Make it work. Make it right. Make it fast.

There's been a lot of talk on how high the quality and polish bar is getting on the App Store in order to succeed. True. Does it have to be as polished on launch though? Sometimes polish and UX are a mask in front of a product that's not that useful anyway.

I'm a big proponent of incremental updates. Ship something good enough to learn from your users, then keep making it better and better.

Upgrading an app written for iOS 7 straight to iOS 11 requires a bit of work. _More on this in another post_. Here are some of the **compromises** I made to ship as soon as I could.

- The nav bar icons are not homogeneous in size. I used custom views, which apparently iOS 11 broke for the `rightBarButton` item (link needed). Had to switch to plain `UIImage` for those. I got them to a point where they're decent enough, will tweak them later.
- The colors of the widget are exactly the same iOS uses.
- For some reason the action sheet shown from the settings sometimes has white tint, others black.
- The swipe on the cell has lost its animation and bounce. I could only get it to work without animating it.


### Room for improvement

Being in touch with the users and getting their feedback is critical to develop a product they'll keep using, and recommend their friends.

I surveyed those users that over time got in touch with me trough the contact features in the app. _More on this on another post_. I got 13 replies out of 183 emails, 7% success rate. Suboptimal for a survey, but good enough for me.

A mistake I made though was to start working on the app before getting results from the survey. What if no one replied? It could have been a fun but pointless exercise.

I live tweeted the process of getting the original Xcode 6 codebase to build in Xcode 9. That was fun and boosted my ego. It was also an utter waste of time. I estimate it took me at least twice as long that way.

### Next steps

The user survey showed some low hanging fruits to deliver a more valuable experience. The easier to tackle is adding bit of visualization on the goal progress and estimated date of achievement.
