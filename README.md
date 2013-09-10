Download-Tracking for google analytics
============================

Adds a simple event based tracking of filedownloads for Google Analaytics.

Requirements
-------------

 * jQuery
 * analytics code obviously

Usage
-----

Add track.js to your page after jQuery.
In case you still use the deprecated synchronous tracking, you can use track_sync_fallback.js which checks what kind of tracking is implemented and falls back to synchronous if _gaq.push is not available.

How it works
------------

A click-event is bound to every link pointing to a .zip or .pdf file.
When clicked a analytics trackEvent - call is initiated.

In Analytics tracking events are structured over Categories, Actions and Labels.
This snippet sets
Category : "download",
Action: filetype
Label: Filename

So any clicks on /static/my_report.pdf will be tracked under: download > pdf > my_report.pdf