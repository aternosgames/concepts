---
description: 'Minecraft server orchestration software targetting on performance and high-scalability'
---

# Impulse \(Minecraft server orchestration software\)

[**Impulse GitHub Repository**](https://github.com/aternosgames/impulse)

## The problem
Nowadays there are a actually lot of products available to manage servers and automate processes and to an extend they
do it actually pretty good. There is Docker in place to virtualize/containerize software, Sentry.io for analyzing and
collecting exceptions that occurred *somewhere*, multiple different webpanels for managing *A*, *B* and *C* and the list
goes on.

The previously named products/solutions are great and all but actually do not solve the problem the Aternos Games project 
has: A server orchestration software that manages a lot of Minecraft servers **and** players with low resource costs, 
high-scalability and state of the art technology and practices. 

Now, there are actually some projects that atleast _try_ to solve the named problem. Whether or not they are successful in
doing so is arguable. To name a few of them: 
* [CloudNet](https://github.com/CloudNetService/CloudNet) _(open source)_
* [TimoCloud](https://github.com/TimoCloud/TimoCloud) _(open source)_
* [CentauriCloud](https://github.com/CentauriCloud/CentauriCloud) _(open source, inactive)_
* [CloudSystemIO](https://cloudsystem.io/) _(paid)_
* [CaveCloud](https://cavecloud.net/) _(paid)_

None of them do solve the problem Aternos Games has so we'll have to develop our own Minecraft server orchestration
software. This is where _Impulse_ comes in place.

## Idea
The idea of Impulse is to provide an easy-to-use orchestration software which is capable of managing a large amount of
Minecraft servers/Minecraft server clusters by automating a lot of processes. Such processes are:
* Start Minecraft servers, either just one or multiple at once
* Restart/Stop Minecraft servers on emergency cases (deadlocks, time-outs, crashed and idling servers)
* Restart/Stop Minecraft servers after a fixed amount of time
* Limit and manage resources dedicated to Minecraft servers

### The daemon
The daemon is designed rather simple compared to all other components of _Impulse_. Short definition of 'Daemon':<br>
> [...] a background process that handles requests for services such as print spooling and file transfers, and is dormant
when not required.

In this case our daemon needs to do a lot more rather than _print spooling_ and _file transfers_. Its job is to:
* Organize and keep hold of a template that represents a Minecraft server which is configured for a task, gamemode or else
