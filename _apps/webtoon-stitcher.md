---
title: "Webtoon Stitcher"
date: 2026-06-29
---

App that helps speed up putting photos together for webtoons.

# 7/5/26

Added a new feature where panels are automatically detected when the user
provides rectangular, marked delineations of where the panels should be. The
color used for the line is specified at the upper right corner. Once the app
recognizes the panels, it automatically does a tight crop to remove excess
whitespace.

<div style="display: flex; gap: 10px; flex-wrap: wrap; align-items: flex-start;">
  <img src="{{ site.baseurl }}/img/markerfeature.png" alt="Marker feature screenshot" style="max-height: 500px; width: auto; height: auto;">
  <img src="{{ site.baseurl }}/img/markerfeaturelines.png" alt="Marker lines screenshot" style="max-height: 500px; width: auto; height: auto;">
</div>

# 6/29/26

Stitches images together, can customize spacing.

{% include video.html src="/img/stitch.mp4" type="video/mp4" %}

Detects panels and stitches them together.

{% include video.html src="/img/detect.mp4" type="video/mp4" %}

Adds captions under each panel. Can paste a bunch of text with delimiters to
denote where caption belongs.

{% include video.html src="/img/captions.mp4" type="video/mp4" %}

Used to make

- [Hungry Gear Throttle Pt. 2](https://www.webtoons.com/en/canvas/aero-gear-throttle/gag-special-episode-hungry-gear-throttle-pt-2/viewer?title_no=1098695&episode_no=26)
- [Rock paper scissors](https://www.webtoons.com/en/canvas/aero-gear-throttle/gag-special-episode-rps/viewer?title_no=1098695&episode_no=27)

editing is now super fast and from phone
