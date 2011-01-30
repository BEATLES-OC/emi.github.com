---
layout: blog
title: More FilteredList examples
author: Daniel Weaver
synopsis: New ajax examples that show what FilteredList is really for.
---

I've added some [AJAX examples](http://emi.github.com/filtered_list) to
[FilteredList](https://github.com/emi/filtered_list) and documented the
options to DataCache. In order to make all the examples work as github-pages
and also slow things down enough that you can see the items showing up in the
UI as they "arrive from the server", DataCache got a couple new options
(letting you use GET for requests instead of being hardcoded to POST, and
letting the delay be specified instead of hardcoded at 50ms). As a bonus I
discovered and fixed a couple minor bugs in the process of writing the
examples.