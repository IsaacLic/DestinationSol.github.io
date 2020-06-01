---
layout: post
title: Google Summer of Code Project!
description: > 
  This is the first post from the GSOC project.
  This summer, I'll build an ECS structure for Destination: Sol.
author: "Isaac Lichter" 
image: "gooey.png" 
parallax: true 
---

Hi everyone! This summer for Google Summer of Code, I'll be refactoring the Destination Sol code to use [Entity-Component-System (ECS) architecture](https://github.com/MovingBlocks/Terasology/wiki/Entity-System-Architecture), so that it'll be easier to build upon and modify. ECS architecture uses composition, rather than inheritance, so that it's easy to add or remove functionality.


For example, in order to construct a ship with a shield, an entity would be given a ship component and a shield component. If, at a later point, the ship loses the shield, then the shield component would simply be removed. However, if the ship with a shield was constructed using inheritance (i.e. the ship-with-a-shield class inherited from ship), then it would be very difficult to remove the shield dynamically.

An ECS library, [Gestalt](https://github.com/MovingBlocks/gestalt), has been constructed for Destination: Sol. I'll be using it to create an ECS-based version of what is currently the SolObject interface. I'll use that to refactor asteroids, ships, and more. 

For more details, look at my [project proposal](https://docs.google.com/document/d/1bUZ0gwnTnsGH8nh6vGR-kSnQQi2JgoltbfyzCiakzyI/edit). My project starts on June 1 and ends on August 24. I'll post here about my progress every other week. The overall status can be found [here](https://trello.com/c/otWA5UdS/129-isaac-destination-sol), and the more detailed status can be found [here](https://trello.com/b/plUYIZ3v/refactoring-ds-to-use-ecs-architecture). My code can be found [here](https://github.com/IsaacLic/DestinationSol).