---
layout: post
title: 'Week Three: Days Four and Five'
date: '2016-01-31T12:02:59-05:00'
tags:
- week 3 day 4
- week 3 day 5
- bitmaker
- bitmaker labs
- hashing
- hashing algorithms
- encryption
- passwords
- coding
- programming
- bcrypt
- rainbow tables
- salting
- cookies
- sessions
tumblr_url: http://karenjho.com/post/138417118227/week-three-days-four-and-five
---
After a couple weeks building apps that were based on only one kind of object or model (e.g. only contacts for our CRM), we finally waded into databases and associations this week. Natalie, one of the other instructors at Bitmaker, introduced us to the Rails method for setting up different models (the tables in a database) and linking them together with associations (the relationships between the tables). See my notes on associations in the latest Today I Learned (TIL) post.In other news, Frank and I finished the Escher puzzle!It is finished. Hallelujah!As we were nearing the end of the puzzle, we realised that there were definitely a few pieces missing. Frank, hero that he is, scoured the house for the missing pieces. He found two of the pieces in corners nowhere near the puzzle. Sock transfer, maybe?On Friday, Mina, our lead instructor, introduced us to user authentication and sessions. User authentication is making sure a user is who they say they are. Sessions allow authenticated users to interact with your application, without re-authenticating themselves every time they do something new (like click on a different link). Can you imagine how annoying it’d be if you had to re-enter your username and password on Instagram every time you liked a photo, posted a comment, loaded a user profile? Sessions are saved as cookies (which you’ve probably seen warnings for, or cleared out of your browser history).User authentication is usually as simple as a username and a password. Sometimes it can even be just a username, if you’re not too concerned with a high level of user authenticity. For the most part, a certain level of authenticity matters and for that reason, passwords are used. But how do you store a password and then prevent hackers from getting into your database and stealing it? Well, you don’t store the password at all.Instead, you store something called a hash. A hashing algorithm will perform a one-way conversion of the password into a digital fingerprint, or hash. This digital fingerprint is always the same for that password. The emphasis on one-way is important, because a hacker cannot convert the hash back into the password.Mina illustrated one-way conversion this way: “I add two numbers together to get 700, and then I ask you which numbers I added together. Given the number 700 alone, you don’t know the two original numbers.”Merely hashing passwords is not secure. Hackers can use rainbow tables to figure out the hashing algorithm, or hash tables to just look up the password if it’s a common one. So, before you hash your passwords, you should salt them, too.To salt is to add a chunk of random data to your password before turning it into a hash. The salt makes a common password uncommon. Hackers then need to have a database for every unique salt + password combo. They would either need much larger databases, or have the computational power to try a list of potential passwords against every stored hash—slower than doing it the big database way. But hashing algorithms are usually pretty quick.With bcrypt, the encryption method most commonly used with Rails, there is one more security measure. Bcrypt is designed to be slow and computationally expensive, which means that any hacker wanting to crack your site needs a lot of time and computing power. The trade-off is that the bcrypt will also run slowly and take up a lot of room in your application, too. So bcrypt allows you to decrease the computational cost to improve your application’s speed and space for a (slightly) lower level of security.I love learning about encryption methods like hashing and salting. (You can also add pepper!) Though I lack the mathematical mind to develop a hashing algorithm, I appreciate the elegance and beauty of well-designed encryption.
