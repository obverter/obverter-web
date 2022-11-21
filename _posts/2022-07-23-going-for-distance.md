---
author: Ben Tyler Elliott
date: 2022-07-25 11:58:47 +07:00
image: "/assets/img/type-two-baseball.jpg"
layout: post
repo: "https://github.com/obverter/going-for-distance"
tags: [baseball, python/pandas]
title: Max Scherzer Could Have Thrown a Baseball Across the Country
---

If Max Scherzer threw every pitch he's ever thrown at 45°, he could've thrown a ball from Cleveland to Seattle.

And then to San Francisco.

<!--more-->

In fact, here's exactly how far he could've gone:


<iframe width='80%' height='400px' src="https://api.mapbox.com/styles/v1/obverter/cl5wpo4yj000a15oagau5m77f.html?title=false&access_token=pk.eyJ1Ijoib2J2ZXJ0ZXIiLCJhIjoiY2w1dHM1YWl5MDRndDNkbW95aWFoNHRiZSJ9.JjyrEbdkcdCpUHLeYoP4IA&zoomwheel=false#3.26/44.24/-102.53/0/9" title="Outdoors" style="border:none; padding:2rem 0 0 0;"></iframe>

For the unfamiliar, Max Scherzer is <mark>extremely</mark> good at baseball.

He can throw a baseball about **a hundred miles per hour**. All day. Every day.

And speaking of days: he almost never has a bad one.

Also, he can **intimidate the skeleton right out of your body**.

<iframe src="https://giphy.com/embed/3xIqGZ2BP2iH22zRiA" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/mlb-max-stare-scherzer-3xIqGZ2BP2iH22zRiA">via GIPHY</a></p>

But I don't care about any of that right now.

Right now, I only care about one thing...

## How far can Max Scherzer throw a baseball?

More specifically, how far would Max travel if he exactly replicated the speed and spin of every pitch in his career to date, but instead went for maximum distance?

If you haven't yet looked at the map a few inches above these words, then the answer may surprise you.

### Max Is My $300 Million Guinea Pig

Since 2008, Major League Baseball has gathered and made publicly available a horrifying amount of empirical data about where and how a baseball moves and behaves on the field.

Every stadium has something like radar installed all around the field, which precisely tracks the movement of the baseball.

*How precisely*, you probably aren't wondering?

Here's the average speed, spin rate, and spin axis of every 4-Seam Fastball that Max has ever thrown:

<iframe title="Max Scherzer's Mean 4-Seam Fastball" aria-label="Table" id="datawrapper-chart-B7D4c" src="https://datawrapper.dwcdn.net/B7D4c/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="186"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

And this is just the tip of the Maxberg.

See, Max made his Major League debut shortly after these systems came online, which means that we have the benefit of having super granular empirical data available for every pitch he's ever thrown in pro ball.

Which got me wondering...

### How Far Can He Go?

I dragged all of Max's pitching data across the Information Superhighway and ran it through the Sausagemaker[^1] in pursuit of a simple question with simple parameters:

1. Suppose I teleport Max Scherzer to a pocket universe that's flat[^2], featureless, and infinite.
2. The atmosphere is set to STP, and there's no wind.
3. Objects don't roll; they stick to the ground exactly where they land.
4. Max can replicate the velocity and spin of every pitch he's ever thrown.
5. He's tasked with throwing each of his historical pitches at exactly 45° up from horizontal.
6. After the throws the first pitch, he walks to where the ball landed.
7. He picks the ball up and throws the second pitch.
8. And then the third.
9. Repeat through all ~44,000ish pitches he's ever thrown.

How far has he traveled?

### Here's Exactly How Far

<iframe title="Max Scherzer's Distance Traveled by Pitch Type" aria-label="Interactive area chart" id="datawrapper-chart-SqjZd" src="https://datawrapper.dwcdn.net/SqjZd/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="600"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

### Fun Facts About His Adventure

1. Max doesn't throw his first Cutter until 2011.

2. Max has thrown only 16 intentional balls in his career, which is bonkers.[^3]
   1. Context: There were two occasions in 2004 when Barry Bonds saw 16 intentional balls in one nine-inning game. Apples to oranges, maybe. But Intentional Walks (which are the product of Intentional Balls) are quite common.

3. Max is almost never told to throw a "Pitch Out," where the manager decides to have the pitcher throw an intentional ball for the sole purpose of giving the catcher a chance to throw out a runner who will probably steal a base. Basically: the manager almost always finds it more advantageous to let Max throw a strike at one thousand miles per hour. Max's pitch velocity and accuracy is so high that a 4-Seam Fastball in the strike zone will reliably accomplish everything that a pitch out is intended to provide: location predictability and pitch quickness so that the catcher has the best possible opportunity to throw out a stealing runner.

---

[^1]: I still can't settle on a nickname for my development environment.
[^2]: Flat meaning he's standing on a flat plane in a three-dimensional space. He's not suddenly two-dimensional.
[^3]: Intentional Balls were phased out of the game a few years ago[^4] — ostensibly to <span style="font-family:Comic Sans MS">**sPeEd uP tHe GaMe**</span>. But this doesn't change much about Max.


---

###### Wanna see how I polished this diamond? Peep the Repo

[Boop This Enormous Button to Head to GitHub](https://github.com/obverter/going-for-distance/blob/master/He's%20Going%20for%20Distance.ipynb){: .btn}

---
