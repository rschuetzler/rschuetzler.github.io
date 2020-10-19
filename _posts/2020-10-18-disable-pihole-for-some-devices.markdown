---
date: "2020-10-18"
layout: post
title: How to disable Pi Hole for specific devices
---

[Pi Hole](https://pi-hole.net/) is awesome for blocking ads on all devices on your local network, but sometimes it gets in the way. Sure, you can log in and disable it temporarily, but for some people that's too much work. Thankfully, updates in the newest version of Pi Hole allow you to turn it off for specific devices. For example, I've disabled blocking on one phone in my house so it can freely click on tracker links and avoid getting blocked by those annoying websites with ad-block detectors.

## Requirements
* Devices to be blocked must have a static IP address (assigned at the router, DHCP server, or device level)
* Pi-hole v5.1 or greater (I think, I know it's not available pre-v5)

## Steps

1. In the Pi-hole web GUI, go to Group Management, then Groups
2. Create a new group. You can call it whatever you want (I called it "Unblocked")
3. Still under Group Management, go to Clients and find the IP address of the device you want to unblock. You can create a comment to remember which device it is if you want.
4. Add the client, then assign it to the Unblocked group.
5. Go to the Adlists under Group Management and check the group assignment for each list in your adlist. You can select all, some, or none of the lists to be applied to your Unblocked group.

That's it! You don't need to change anything on your device. By default, the new settings should start working immediately, and you can view all the ads you want on devices in the Unblocked group.
