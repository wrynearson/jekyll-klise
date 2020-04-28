---
title: Maps of Buildings
date: 2020-04-28 20:00:00 +02:00
tags: [Maps]
description: Using Microsoft's building dataset to create an artistic map of my hometown
# image:
layout: post
published: true
comments: true
---
{::nomarkdown}
<img 
    src="/assets/img/2020-04-28-building-map-bainbridge/Bainbridge-1.svg"
    alt="Bainbridge Island's buildings" />
{:/}

![Bainbridge Island](../assets/img/2020-04-28-building-map-bainbridge/bainbridge-1.jpg)

I've always loved maps. The differet ways we represent the physical world on a small screenor piece of paper is fascinating. I could spend hours looking at subway maps, old world maps,or beautiful topo maps. They're such a powerful mix of technical prowess and art (maybe that's why I love photography).

Maps, and other visualizations, are a great way to turn complicated or abstract information intosomething understandable. Early on my journey to learn how to visualize data, I've been incrediblyinspired by recent works of data journalism, especially from the New York Times.

The headline for the 2018 piece [*A Map Of Every Building In America*](https://www.nytimes.com/interactive/2018/10/12/us/map-of-every-building-in-the-united-states.html)definitely caught my eye. After reading through, mesmerized by the tiny black dots, I found [Microsoft's Github pepository](https://github.com/Microsoft/USBuildingFootprints/) of **125,192,184** "computer generated building footprints in all 50 US states." What a fascinating way to see our built environment in clarity, without the clutter which comes fromsatelite images or standard online maps.

I'm from Bainbridge Island (near Seattle), so I thought I'd start there. I found [`Washington.zip`](https://usbuildingdata.blob.core.windows.net/usbuildings-v1-1/Washington.zip) file (675 MB) conveniently listed, downloaded it, and loaded it into QGIS.

*Screenshot of Washington.zip in QGIS*

Very new to QGIS (I'm sure there's a better way of doing this), I zoomed into Puget Sound and used the `freehand select` tool to select just the polygons (buildings) on Bainbridge Island. Being an island surrounded by water, as all islands tend to be, it was easy to define what was a building on Bainbridge and what wasn't. Sadly the buildings aren't labeled, unlike how they are in OpenStreetMap.

*Image/GIF of me selecting the buildings on Bainbridge*

I then copied these polygons into a new virtual layer and went to artistic "work" simply changing the background color, fill color and border color. I used a black background and the same color for both the building fill and border, but put the fill at 75% opacity.

![Downtown](../assets/img/2020-04-28-building-map-bainbridge/bainbridge-2.jpg)

Et voilà, it turned out pretty well!

![Nature Reserve](../assets/img/2020-04-28-building-map-bainbridge/bainbridge-3.jpg)

It's interesting to see where the island has been developed, versus where it hasn't. The [downtown](http://wrynearson.github.io/../assets/img/2020-04-28-building-map-bainbridge/bainbridge-2.jpg) area is just north of Eagle Harbor, while the void in the middle is [Gazzam Lake Nature Preserve](../assets/img/2020-04-28-building-map-bainbridge/bainbridge-3.jpg).
<!-- note - full link to see if popup works -->

You can play around with an interactive version using the qgis2web plugin to export it with leaflet [here](/TestMap).