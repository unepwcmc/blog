---
layout: post
title: "Polybri - Realtime web polygon editing"
date: 2011-04-14 21:22
comments: true
categories:
tags: node.js 
author: Craig Mills
---

<p>We've been playing with <a href="http://nodejs.org/">node.js</a> with <a href="http://nowjs.com/">now.js</a> this week to put together a collaborative browser based polygon editor we're calling <strong>'Polybri'</strong></p>
<p><img src="/images/polybri.png" alt="Polybri screenshot"/></p>
<p>The app syncs a polygon between users as they edit them in real time. <a href="http://nowjs.com/">Now.js</a> is used to pass chat messages and GeoJSON between clients.</p>
<p>When user are finished editing, they can save their maps, which are then displayed with <a href="http://polymaps.org/">Polymaps</a> on the homepage</p>
<p>You can check out the code over at our <a href="https://github.com/unepwcmc/polybri">Github Repo</a></p>

