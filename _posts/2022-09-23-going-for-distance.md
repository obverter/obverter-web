---
author: Ben Tyler Elliott
date: 2022-09-23
image: "/assets/img/posts/going-for-distance/maxinator.png"
layout: post
published: true
repo: "https://github.com/obverter/going-for-distance"
tags: [baseball, python/pandas]
title: Max Scherzer Could Have Thrown a Baseball Across the Country
---

If you run the numbers for his career-to-date, Max Scherzer could've thrown a ball from Cleveland to Seattle.

And then to San Francisco.

<!--more-->

## Going For Distance

{% marginnote 'mn-1' "These are the things I wonder about while I'm <a href=\"http://www.obverter.com/type-two-baseball/\">watching baseball</a>." %} I was watching Scherzer pitch and I wondered: how far would Max travel if he exactly replicated the speed and spin of every pitch in his career to date, but instead went for maximum distance?

Like, what if instead of throwing each of those pitches toward the strike zone, he instead yote{% sidenote 'sn-1' 'yote. *v.* simple past tense of **yeet**.' %} them toward the horizon at a 45˚ angle, and then walked to where the ball landed, picked it up, and uncorked the next one, and so on?

TL;DR — About this far:

<iframe class='iframe' min-width='600' height='600' src="https://api.mapbox.com/styles/v1/obverter/cl5wpo4yj000a15oagau5m77f.html?title=false&access_token=pk.eyJ1Ijoib2J2ZXJ0ZXIiLCJhIjoiY2w1dHM1YWl5MDRndDNkbW95aWFoNHRiZSJ9.JjyrEbdkcdCpUHLeYoP4IA&zoomwheel=false#3.26/44.24/-102.53/0/9" title="Outdoors" style="border:none; padding:2rem 0 0 0;"></iframe><br>

## I'm Going to Need Some Data

Handy for me: since 2008, Major League Baseball has gathered and made publicly available a horrifying amount of empirical data about where and how a baseball moves and behaves on the field.

Every stadium has something like radar installed all around the field, which precisely tracks the movement of the baseball.

*How precisely*, you probably aren't wondering?

Enough for me to say with absolute certainty that this is the average speed, spin rate, and spin axis{% sidenote 'sn-1' "From the batter's perspective." %} of every Four-seam Fastball that Max has ever thrown:

|                    |  Speed |      RPM | Spin Axis |
|:-------------------|-------:|---------:|----------:|
| Four-seam Fastball | 94.337 | 2490.361 |  217.370˚ |

And Max is the perfect candidate for this waste of time, too. Aside from being one of the greatest pitchers of his generation, he made his Major League debut shortly after these ball-tracking systems came online. This means that we have super granular empirical data available for every pitch he's ever thrown in pro ball.

## So Let's Set Some Parameters

I'm going to assume that Max is going to throw every pitch with the same speed, spin rate, and spin axis as he has in his career to date. He's going to repeat the first throw from his career, walk to where the ball lands, and then repeat the second throw of his career, and so on, until he's replicated all ~44,000 of his career's pitches to date.

I'm also going to assume that he's performing this feat under these conditions:

| Parameter          | Pocket Universe |
|:-------------------|:----------------|
| Topography         | Flat            |
| Atmosphere         | STP             |
| Wind               | Nope            |
| Launch inclination | 45˚             |

Also, I'm going to make my life about infinity easier by assuming that the ball is going to travel in a straight line, and that it doesn't bounce or roll when it lands.

## How Far Can He Go?

Here's approximately/exactly how far:

| Pitch                |      Count | Mean Distance (m) | Approx. Total Distance (m) |
|:---------------------|-----------:|------------------:|---------------------------:|
| Four-seam            |     23,967 |            128.18 |                  3,100,000 |
| Sinker               |        526 |            119.09 |                     62,600 |
| Curveball            |       2593 |             97.04 |                    251,600 |
| Change-up            |       7307 |            102.50 |                    749,000 |
| Cutter               |       1512 |            131.40 |                    199,000 |
| Slider               |       7868 |            108.85 |                    856,500 |
| :------------------- |    ------: |    -------------: |             -------------: |
| **Total**            | **44,023** |        **111.96** |              **5,218,700** |

About 5.2 million meters, or 3.2 million yards, or 1.8 million miles.

Wait, that can't be right.

$$
\begin{array}{rcl}
1000\ m & = & 1\ km \\
 & = & 0.6214 \ mile \\
\end{array}
$$

$$ \frac{5.2\times10^6}{1000}\times 0.6214 = 3231.28 $$

About 3231.28 miles, more or less.

Or, roughly the distance from Cleveland to Seattle to San Francisco.

## Peep the Repo

This silly little thought experiment turned out to be way harder than I thought it'd be. If you're interested in a deep dive into the code and/or watching me claw my way through a bunch of horrifying{% sidenote 'sn-3' 'To me, anyway.' %} undergraduate physics, you can find it here:

[Boop to Head to GitHub](https://github.com/obverter/going-for-distance/blob/master/He's%20Going%20for%20Distance.ipynb)

But just for funsies, here's a quick look at the data I generated for just one pitch:

| Key           |      Value |
|:--------------|-----------:|
| mph           |       95.7 |
| theta         |       45.0 |
| omega_rpm     |     2400.0 |
| backspin      |       True |
| y<sub>0</sub> |     1.7081 |
| omega_radsec  |   251.3274 |
| vt_msec       |    42.7725 |
| vx            |    22.4693 |
| vy            |    36.3953 |
| vr_mph        |    20.7065 |
| vr_msec       |     9.2563 |
| spin_factor   |     0.2164 |
| coeff_drag    |     0.0032 |
| drag_force    |    -0.0152 |
| coeff_lift    |     0.2298 |
| magnus        |     1.0972 |
| f<sub>x</sub> | -8958.1117 |
| f<sub>y</sub> | 5147.09799 |
| k             |     3.7846 |
