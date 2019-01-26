---
layout: post
title:  "Discord Bot"
subtitle:  "A web scraping Discord bot written in node.js"
desc:  "A bot that scrapes the official Rocket League news site and relays posts to a Discord channel."
date:   2018-07-15 00:00:00 +0000
categories: project node.js javascript bot
---

This is my first project using [node.js](https://nodejs.org) and was created for use in a small sized Discord community of Rocket League players. We found ourselves linking the [official blog posts](https://www.rocketleague.com/news/) every time a new one was released for us to discuss the changes however this relied on us spotted them meaning many would be delayed or go missed altogether, this triggered my quest to automate the process.

At set intervals the bot checks the news index page to see if any new posts appear. The results of this is then checked against a local sqlite database. Once a new post is found the web page for that blog post is parsed to get further details.


The image from the blog post is downloaded and analysed where the five main colours are ranked by frequency and luminance the second highest scoring colour is then used within the Discord embedded message, a small detail that could easily go unnoticed.

The above colour along with the title, description, author, categories, and tags are unified into an embedded Discord post. The bot then utlises the [discord.js](https://discord.js.org) module to interact with Discord and sends a message to a specified channel.


**Example Post**    
![]({{ site.url }}/assets/images/rocket_league_bot_preview.png)

**Reflections**    
As one of my first javascript projects the code although functional is still rather messy which is something I wish to refactor in the future.  Having to work with async methods using requests and promises was also an interesting concept that caused a lot of the above mess.

The data within the system isn't persistent as the bot is hosted using [Heroku](https://heroku.com) another tool that I had not used prior to this project which could cause issues when the bot restarts as the sqlite database is cleared. To combat this an initial scrape is carried out which is used as a base to test new posts against which could mean posts during restarts do not get posted.
