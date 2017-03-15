---
layout: post
title:  "Avatar Item Remove"
subtitle:  "Editing Web Content with an Extension"
desc:  "An addon that replaces user avatars with a more generic image."
date:   2015-03-14 18:26:33 +0000
categories: project html css
---
Viewing online forums around family and friends can often be tricky with many sites allowing users to configure their own profile image to whatever their heart desires, to save myself from any embarrassment I created a solution. Rather than removing avatars completely I wanted to replace them with something a little more generic as this would still allow the user to recognise individuals based on their appearance.

I created a Chrome Plugin that finds all elements matching an avatar which then generates them a new default one using an SVG image that is given a colour based on the users name so their avatar is consistent.

This was my first go at creating a Chrome Plugin, the format of the code also doubles as a great TamperMonkey script. Allowing those who want to use the extension to install it with ease.

![]({{ site.url }}/assets/images/avatar_remove.png)

Source: [AvatarItemRemove Github Repo](https://github.com/Pugzy/AvatarItemRemove)
