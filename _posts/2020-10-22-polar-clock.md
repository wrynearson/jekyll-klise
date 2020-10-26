---
title: Polar Clock
date: 2020-10-22 10:55:00 +02:00
tags: [Dataviz]
description: Test
layout: post
published: false
comments: false
---

This is a polar clock I edited from [this](https://observablehq.com/@mbostock/polar-clock):

<div class="chart"></div>

<script type="module">
import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
import define from "https://api.observablehq.com/d/e590bef5c3cb1d06.js?v=3";
(new Runtime).module(define, name => {
  if (name === "chart") return Inspector.into(".chart")();
});
</script>