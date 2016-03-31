---
layout: post
title: 'Week Two: Day Four'
date: '2016-01-21T22:39:37-05:00'
tags:
- week 2 day 4
- bitmaker
- bitmaker labs
- coffee and code
- grilled cheese
- html
- css
- ruby
- coding
- programming
tumblr_url: http://karenjho.com/post/137790407855/week-two-day-four
---
On Tuesdays and Thursdays, we have Coffee and Code sessions at 9am. Ilia, one of the instructors at Bitmaker, leads us through some short exercises to stretch our Ruby muscles. What has excited me most about these sessions are the nth different solutions to a particular problem, and how those solutions reveal the way a solver thinks. I love working through the problems, and then seeing how another tackled it with a divergent method.Here’s a small sample problem (my solution is at the bottom of the post):Create this array in Ruby:[1, 12, 144, 1728, 20736, 248832, 2985984, 35831808]Also, today was Grilled Cheese Thursday, y’aaaaaaaaaaaall. My love of cheese can only be matched my digestive system’s incompatibility with cheese. But I will hold in my farts all afternoon for a taste of that sweet, sweet cheddar.Ella, one of the staff at Bitmaker, making grilled cheese sandwiches for Team Gort. Thanks, Ella!This afternoon, I finally cleaned up the rest of my CSS layout. My little address book is now an address book on the web. Well, at least it’s on the web whenever I launch my web server with Sinatra. I have dubbed my little project “Layer Cake” so it might sound more delicious and enticing. The jury’s still out on the name.Now the work is to tie the front-end (all the pretty and not-so-pretty HTML and CSS) to the back-end (the diligent Ruby), and make sure that the information the user inputs actually goes where it’s supposed to. That’s the part I’m stuck on now. There have been one too many “undefined method” errors for the night. I’m going to ask for help tomorrow.My solution to the Coffee and Code problem: (0..7).to_a.map { |num| 12**num }
