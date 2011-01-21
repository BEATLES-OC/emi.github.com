---
layout: blog
title: EMI's public repositories
author: Daniel Weaver
synopsis: Presenting a new jQuery plugin and an update to an old (abandoned?) Java ID3 library
---

Our products would be impossible without open source software; Merb, jQuery and MySQL form the core of
our technology stack, augmented with dozens of plugins, gems and assorted libraries. The breadth and
quality of these freely shared pieces of code let us focus our efforts on the problems specific to our
applications. So it is with some pride (and relief!) that we are publishing our first jQuery plugin,
[Filtered List](http://emi.github.com/filtered_list) including an
[example](http://emi.github.com/filtered_list).

We have a couple places in our apps where we want to show a long, scrollable list of items, where
basic information about each item is cheap to calculate but the fully populated item requires an extra
query or two. Since it is a long list, we want users to be able to quickly filter the results with a
search term or two, and when items are displayed we want to decorate them with all of their
information. Filtered List initializes quickly, allows searching against all the information at hand,
and prioritizes its ajax requests to complete the items the user is looking at first. It comes with
Jasmine unit tests and some Ruby scaffolding around so those tests can be a CI environment;
specifically, our CI environment, but hopefully yours too if you choose to hack on Filtered List. It
is available under the usual jQuery plugin licenses.

The other project is [JID3](https://github.com/emi/jid3), a Java library for manipulating ID3 tags in
MP3 files [written by Paul Grebenc and last updated in 2005](http://jid3.blinkenlights.org/). We like
this library because it can modify a file on the fly while streaming it. To our surprise, however,
Unicode tags created on our Linux servers were flagged as being corrupt by Windows Media Player (up
through at least version 11). This is due to a bug in WMP; it violates the ID3 spec and cannot handle
big-endian UTF-16. Regardless, it is much easier for us to patch JID3 on our servers than to patch
Windows Media Player and distribute it to every PC in the universe (or at least the handful that
haven't installed iTunes). So that is what we did. JID3 is distributed under the LGPL.
