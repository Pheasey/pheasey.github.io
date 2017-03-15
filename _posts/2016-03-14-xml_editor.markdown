---
layout: post
title:  "PGM XML Creator"
subtitle:  "Creating XML from user inputted Data"
desc:  "Using Javascript and Bootstrap CSS to output XML."
date:   2015-03-14 18:26:33 +0000
categories: project html css js
---

A Minecraft server that accepts community submitted maps required XML files to provide the server with data such as spawn points and objectives. To make this easy for map developers I created a simple form solution which would allow them to enter their maps data and generate the XML automatically.

I created this site using [Bootstrap](http://getbootstrap.com/) CSS and Javascript for collecting and formatting entered data.

![]({{ site.url }}/assets/images/pgm_xml.png)
Live Demo: [XML Creator](http://pugzy.github.io/XmlCreator/)

An example XML can be seen below.

```
<?xml version="1.0"?>
<map proto="1.4.2">
<name>Viridun Headquarters</name>
<version>1.4.8</version>
<objective>Be the team with the least amount of deaths after 10 minutes.</objective>
<authors>
    <author uuid="27cf0cdd.." contribution="Map design and layout"/> <!-- OurLoneHero -->
</authors>
<contributors>
    <contributor uuid="82c796a5.." contribution="Map design"/> <!-- IM_A_H0B0 -->
    <contributor uuid="97abb45c.." contribution="Design"/> <!-- ander301 -->
</contributors>
<teams>
    <team id="blue-team" color="blue" max="40">Blue</team>
    <team id="red-team" color="dark red" max="40">Red</team>
</teams>
<kits>
    <kit id="spawn-kit">
        <item slot="0">stone sword</item>
        <item slot="1" enchantment="arrow infinite:1">bow</item>
        <item slot="28" amount="1">arrow</item>
        <item slot="2" amount="16">cooked chicken</item>
        <item slot="3" damage="8229">potion</item> <!-- potion of instant health 2 -->
        <item slot="9" damage="4">ink sack</item>
        <potion duration="10" amplifier="1">heal</potion>
        <potion duration="20">damage resistance</potion>
        <chestplate locked="true" unbreakable="true">elytra</chestplate>
        <double-jump power="10" recharge-time="30s" recharge-before-landing="true"/>
    </kit>
    <kit id="red-kit" parents="spawn-kit">
        <helmet color="cd0000">leather helmet</helmet>
        <leggings color="cd0000">leather leggings</leggings>
        <boots color="cd0000" enchantment="protection fall:2">leather boots</boots>
    </kit>
    <kit id="blue-kit" parents="spawn-kit">
        <helmet color="0066cc">leather helmet</helmet>
        <leggings color="0066cc">leather leggings</leggings>
        <boots color="0066cc" enchantment="protection fall:2">leather boots</boots>
    </kit>
</kits>
```
