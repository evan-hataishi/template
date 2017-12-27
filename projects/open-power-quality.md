---
layout: project
type: project
published: true
image: images/opqbox-2.5.jpg
title: Open Power Quality
permalink: projects/openpowerquality
date: 2017
labels:
  - Raspberry PI
  - Python
  - MongoDB
summary: Open source hardware, software, and data for low cost, crowd-sourced power quality monitoring, storage, and analysis.
---

<img class="ui medium right floated rounded image" src="{{ site.baseurl }}/images/opqbox2.JPG">

The Open Power Quality project explores open source hardware, software, and data for low cost, crowd-sourced power quality monitoring, storage, and analysis.

In Hawaii, the high cost of energy combined with federal and state subsidies for photovoltaic installation has led to increasing penetration of distributed, intermittent generation in the grid. However, the impact of this change on power quality is not well understood.

### How I met the OPQ team ###

I first joined the OPQ team in August of 2017. I had initially heard of the
project during the Spring semester when coming in for help from my operating
systems TA, Serge. I noticed he had a bunch of cool tech laying around his
office. There were just a bunch of plugged in Rasberry PIs, but I had never used
one before. When I asked him about them, he suggested that I come talk to him
over the Summer to talk about his work and see if there would be something for
me to do on the project. Eventually, towards the end of the Summer, I came into
contact with Professor Johnson and the rest of the OPQ team, where they quickly
ramped me up to everything on the project, and I've been helping them out with
it ever since.

### My first project - OPQ package updater ###

Since the plan is to eventually have the OPQ boxes distributed all around the
island (most of them are currently in POST and some of the OPQ team's homes),
we needed a way to update the boxes securely and remotely. After a lot of
research and trying different libraries out, we ended up with [this](https://github.com/openpowerquality/opq/tree/master/box/Software/Updater).

1. Download the version file (contains latest update info) from an OPQ server
1. Compare the version file to the boxes local version file
3. Download the public key, update package, and signature
4. Verify the update package with the key and signature
5. Unzip the update package
6. Run the script file

### Uptime analysis ###

Most recently, I've been looking into some of the data that our boxes collect. Everyone thought it would be a good idea for me to get my feet wet in our data and database structure by doing some data analysis myself. Serge thought it may be useful for to have a tool that could run through all our data to find times where boxes may have been down by calculating uptimes between each record. Just scanning through the first 5000 records already yielded interesting data and provided us with insight on when our devices go down for large periods of time.
