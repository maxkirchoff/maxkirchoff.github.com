---
author: max
layout: post
title: "Badass LAMP stack in 10 minutes"
date: 2013-02-12 14:06
comments: true
categories: 
- LAMP
- Ubuntu
- VPS
- Cloud Servers
- PHP

---

While lamenting my personal VPS today, [Sam](https://github.com/samkeen) nonchalantly mentioned the hot new [DigitalOcean](https://www.digitalocean.com/) that was being vetted on [hacker news](http://news.ycombinator.com/item?id=5207162) as a suitable challenger to [Linode](http://www.linode.com/). Ignoring Sam's recommendations is a geek "faux pas" as he's the *go-to early adopter* of cool projects and services. As such, I jammed over to **DigitalOcean's** site to sign up. 

Their Trial Account option had been locked down due to the massive response they were recieving - probably a mixture of **"cha-ching!"** for thier business team and **"oh shit!"** for their tech team. 

### $5 Server Value Meal

By providing a credit card I was able to get an account on their smallest machine at a meager $5/mo. Yes, $5. Five bucks. For the price of commuting to work on the train for one day, I got a SSD server.

To backup a little, if you're not familiar with Linode, DigitalOcean, or that class of VPS service, these are the perfect place for small projects, blogs, simple sites, and beta testing grounds for new ideas. They offer actual server ownership so you can configure and deploy MANY types of systems and stacks without cost of bigger services or the overhead of fulltime system administration. 

### Server Building in 10 minutes
Right away DigitalOcean's admin UI made sense to me. Create a Droplet (just think of this as a server for now), take snapshots of a Droplet, manage DNS, manage billing. 

My initial Droplet was configured as such:

* Droplet Size: 512MB RAM, 1 CPU , 20GB SSD Disk
* Droplet Location: New York
* Droplet Image (OS): Ubuntu 12.10

With these selections I could replicate my Linode VPS and quickly get my code moving. Build and boot of my Droplet was roughly **55 seconds** (just as they advertise).

I didn't follow their [Ubuntu setup guide](https://www.digitalocean.com/community/articles/initial-server-setup-with-ubuntu-12-04), but it's really well written. If you don't know much about managing servers, please read and follow ALL their docs…you will be sorry if you don't.

They emailed me a root password along with a note that my Droplet had been built. I generated some SSH keys and shoved the public key onto the server. I also disabled the password login for root, all about **2 minutes**.

I ssh'd in, updated my system, and started grabbing all the packages I needed. Disk write speeds and downloads were crazy fast. I had apache2, mysql, php5 and all the modules I could carry in about **7 minutes**. 

They offer a great [LAMP on Ubuntu guide](https://www.digitalocean.com/community/articles/how-to-launch-your-site-on-a-new-ubuntu-12-04-server-with-lamp-sftp-and-dns) as well.

I added some folders to `/srv/www` for my sites, configured the vhosts and away we went. Empty Droplet to functioning LAMP stack in 10 minutes flat.

### Take a Snapshot, it will last longer
As with Linode and a few others, backups are available in addition to images. However in DigitalOcean the snapshot/image workflow made more sense to me. Once I had finished my initial LAMP stack setup, I was able to take a snapshot in the admin. With that snapshot I could deploy that image over and over. Obviously with a regular ol' LAMP stack this isn't all that innovative, however with more complicated configurations that involve varying access security and addons (php modules, ruby gems, python dependencies) in a given server environment. 
This also has obvious uses around scaling across multiple Droplets as well.


That's all. Functioning, replicable server is 10 minutes. :P




