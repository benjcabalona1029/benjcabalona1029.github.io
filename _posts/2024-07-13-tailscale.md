---
title: Getting Started with Tailscale
date: 2024-07-13 12:00:00 +8
categories: [Data Science]
tags: [projectcauchy]     # TAG names should always be lowercase
---

Tailscale is my service of choice to giving the mentees access to VMs in my homelab. It's an easy to use solution. I can whitelist precisely which machines I want them to access without exposing my entire network. Setting up tailscale is as easy as follows:

1. Create an account via  [https://tailscale.com/](https://tailscale.com/)
2. Download tailscale into your machine using [https://tailscale.com/download](https://tailscale.com/download)
3. Wait for the invite link that i will send you to access the VM.
4. Test if you can ping the VM.

If the set up is correct, when you navigate to [https://login.tailscale.com/admin/machines/](https://login.tailscale.com/admin/machines/) then you should see something similar to the image below. The one tag as `Shared In` is the machine/VM that I shared. The other is most likely your machine.

![alt text](/assets/images/post_0002/tailscale.png "tailscale")

And that's it!

Learn more about tailscale here:
{% include embed/youtube.html id='sPdvyR7bLqI' %}
