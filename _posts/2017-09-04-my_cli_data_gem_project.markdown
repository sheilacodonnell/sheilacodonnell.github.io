---
layout: post
title:  "My CLI Data Gem Project "
date:   2017-09-04 16:03:27 +0000
---


Finishing my CLI Data Gem Project has been the most rewarding experience thus far. I did it! I built something! Overall, It wasn't as bad as I though it would be. I was pretty nervous leading up to the project, but once I realized what they wanted, my fears subsided.

It turns out, this app doesn't need to be creative, inventive, or even that useful. You're just learning how to build a small CLI app and scrape some info from another website properly. Also, no one (aside from you and the instructor who reviews your app) is going to use this. The chance that someone will want to view the New York Times Bestseller list on a Command Line? Pretty slim. 

This project reminds me of the very first simple HTML/CSS website I built. Was it pretty? No. Was it cool? No. Is it on my portfolio? No. Did it teach me a ton? Absolutely. 

After perusing some blogs, I came across the recomendation to use a website built on Ruby on Rails.  searched a lsit of Rails websites and found Goodreads. I decided to scrape their bestseller list. Later in the project, I found that their HTML/CSS was pretty messy. A lot of class and ID names that were not intuititve, and I was spending a lot of time on something that wasn't really enforcing the objectives of the project. I decided to forego the RoR requirement (and after chatting with other students, realized for a project this simple, using a Rails site doesn't really matter). Instead I checked out the NYT website. Ahhh, beautiful and clean code. If you haven't started your project yet, learn from this! Inspect element before you choose a website to scrape. This is your first project. Make your life easier by choosing a website with nice clean code and tags that make sense.  

In a nutshell, here's how the app works:

- A CLI for bestsellers from New York Times Bestsellers.

- User types in 'books' and a numbered list of books names will then come up. Users can enter a number to get a description of the book. 
 1. Six of Crows 
 2. Loving Frank
 3. The Perfect Game 

Which book do you want to learn more about?
- Enter number and receive more info: title, author, description, and duration (number of weeks the book has been on the list).

I watched all of the videos provided for the CLI project. They were extremely helpful. I coded along, and adjusted my code. One of the biggest stumbling blocks I faced, was an empty array. My list of 25 books, was returning a list of 26...with an empty space on number 26. I played around with so many methods. .pop, .split, and more, trying to eliminate that last array. However, those were not addressing the underlying issue. I wanted code that was flexible and would ajust for any number of books and would know the correct amount of books. I still don't know where exactly the problem was coming from. My scraper code was repetitive, and I decided to shift gears and tighten up the code overall. Somewhere along the line, that fixed my problem. 

Upon checking out the projects from other students, I've learned even more about how many different ways you can do something in Ruby, and how I can make my code more consise. This was a big step forward for me, and I can't wait to find out what my future projects will teach me. 




