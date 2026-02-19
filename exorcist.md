---
layout: default
title: eXorcist RPG
---

eXorcist is an RPG in development with RPG Maker MZ and my own assets. These are
notes for my future reference and a progress log.

# Plugins

## QPlugins for MZ

Need for pixel-perfect movement and collision as opposed to tile-based, which
feels very clunky. [Original](https://quxios.github.io/plugins) Q-Plugins only
works for MV, and not maintained.

Plugin installation instructions
[here](https://forums.rpgmakerweb.com/index.php?threads/lunatechs-mv-mz-plugins-tools.127082/page-5#post-1181837)

Repo [here](https://github.com/LunaTechsDev/Luna-QPlugins/releases)

Add the collision map like this:

{% include image.html src="/img/cm_tutorial.png" alt="Add collision map like this" width=75 %}

## OrangeMapshot for MZ

Exports image of map. Helpful for making collision maps.

Pastebin [here](https://pastebin.com/yatW19nk)

## Cyclone Tile Priority

Need in order to layer the player above the tile when in front, and below the
tile when behind. Sorts using y-coordinate depth. Plugin available with
instructions [here](https://hudell.itch.io/cyclone-tile-priority)

# Progress Log

## 2/18/26

Progress

- Made station bigger
- Set up the "I should sit and wait" event

Event icon: {% include image.html src="/img/events.png" alt="events" width=5 %}

Remaining

- Figure out how to make liminal
- Text prompts while walking
- Address cruft herald sq map debug
- kiosk: eta is delayed
- bench: sit and wait?
- sitting: procs a cutscene

sit and wait:
{% include image.html src="/img/sit_and_wait.png" alt="sit and wait" width=75 %}

cruft:
{% include image.html src="/img/heraldsq_cruft.png" alt="cruft" width=75 %}

Ideas for liminal

- Ripple effect?
  https://toshaangel.itch.io/screen-effects-plugin-for-rpg-maker-mz
- Animated tiles?

## 2/16/26

Happy new year

Immediate work items

- station needs to be bigger and gradually more liminal/odd
- text prompts while chc in motion (optional)
- kiosk: eta is delayed
- bench: sit and wait?
- leaving: "I should just sit and wait"
- sitting: procs a cutscene

## 12/28/25

- Made movement pixel-perfect
- Herald Sq map has pixel-perfect collision and prioritized tiles.

Herald Sq map in collision map debug mode:

{% include image.html src="/img/exorcist_collision_map.png" alt="Collision map" width=75 %}
