---
layout: post
title: "Questions"
date: 2026-01-24
---

### How does machine connection by name look-up work?

e.g. `ssh name`

`DNS` maps the human readable name to an ip address.

look up procedure is specified in a `/etc/nsswitch.conf`

### How does connection by IP address work?

kernel looks at routing table. If found, then target is in local network.
Broadcasts an ARP, asking for MAC.

Not found, then sends to router. Router will know where to send.

You typically trust everyone in the local network. Between routers is usually
authenticated, no trust.

### what is a network interface

piece of hardware that sends and receives packets and connects your machine to a
network. each interface has a MAC address.

eth0 and eth1 could be different devices entirely or same device different
ports.

## what are common kernel utils for network stuff

## what are the resources available on a server, what are their units of

measurement?

## how do you profile these? (ideas for experiments)

## how do you get an intuition about speed and resource utilization?
