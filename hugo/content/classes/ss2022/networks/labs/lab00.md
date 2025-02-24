---
title: Lab 00 - Intro
author: kleinen
draft: true
---

** update 21.10.2021: nur bis 1c bearbeiten, so weit wie Sie im lab gekommen sind.**

## Part 1: Playing with Web Servers

As the Web and Web applications are a central part of networked applications,
we will use the time before really getting started to play around with basic
web servers.

You should be able to do most or all of this with your own computers.
We will build Teams during the first lab, but feel free to start working
on the exercises

### 1.a Simple Web Server in Java: NanoWebServer

Have a look at these examples of very simple webservers implemented
in Java:
[https://github.com/htw-imi-networks/lab00-nanoHttpServer](https://github.com/htw-imi-networks/lab00-nanoHttpServer)

Build in something new, tinker a bit...
for example, try doing a [redirect](https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections)
for an arbitrary new filename (it might be http://localhost:5005/redirect)
that performs a redirect to some other page using the status code 301 "Moved Permanently"

### 1.b Playing with Nginx

Nginx is one of the most popular Web Servers.
Try installing and configuring it on your own computer, or preferably any *nix
computer you can find one.

https://nginx.org/en/docs/beginners_guide.html

The bored can give docker a try:
[https://www.docker.com/blog/how-to-use-the-official-nginx-docker-image/](https://www.docker.com/blog/how-to-use-the-official-nginx-docker-image/)

### 1.c Setting up a real server on a virtual machine

We will do this part together in lab, where I will provide each group with
a virtual server hosted at the HTW - you will install and configure nginx
on port 80 on these machines.
** update 21.10.2021: nur bis 1c bearbeiten, so weit wie Sie im lab gekommen sind.**


~~##### 2. Wireshark Lab: Getting Started~~
** moved to lab 01 **

### Lab Report

Prepare a Lab Report together as PDF structured like this Lab Assignment.
You may work on the reports in flexible teams of 2-3 students.

Always put the names of all contributing people on your report.

** put your server name in your report! **

Each one of you has to hand in the completed Report individually in moodle
by Friday 17:00 after your lab meeting!

In your report, describe what you did and what you found,
 as well as errors or problems you've encountered.
