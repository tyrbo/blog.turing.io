---
title: The Pivot - Airlift
date: 2014-09-26 23:10 UTC
tags:
author: Team Airlift
layout: post
---

## Introducing: The Pivot

The Pivot was the first project we've worked on where the code was inherited 'legacy' code. Working with legacy code (and someone else's code) introduced some unique challenges to overcome.

The idea behind The Pivot was taking an existing site (think Grubhub, but with a single restaurant) and modifying it to support multi-tenancy (multiple businesses interacting with multiple users). In addition, we needed to adjust and modify features as necessary to change from an online food ordering service to a disaster relief service, ensuring that those in need are able to obtain the supplies they require.

## Airlift: The Challenges

One of the earliest challenges we faced was a lack of test coverage for the project. As a result of the minimal test coverage, we felt a bit frightened that making changes or adding new features would end up causing even more problems. Luckily, [Allison](https://twitter.com/allielarson1212) was able to add a significant amount of tests overnight which helped alleviate a bit of the fear we all felt.

We found that a lot of the authorization you would expect was missing from the project we inherited. One of the biggest security holes that we discovered was the ability for a User to change the total price of an Order while checking out. It took some time to really dig around the source code and weed out any other potential vulnerabilities.

Privacy was something that was also important to us. As a group, we concluded that a User could potentially buy items from multiple Suppliers. We also concluded that it didn't make sense for a Supplier to view any information about orders which were not directly related to them. This led us down a path on separating Orders (which is directly connected to a User) and SubOrders (which is directly connected to a Supplier). Trying to determine the best way to implement that system (from a coding standpoint) is something that took a little bit of time to figure out. However, implementing the system in that way allowed us to add a degree of privacy between Users and Suppliers.

## The Good Parts

As a team, we decided from the beginning that collaboration and a smooth Github workflow was very important.

[Jonmichael](https://twitter.com/tyrbo) took on the role of gatekeeper, which meant that any code on it's way to the master branch would first be vetted and approved prior to being merged in. Taking this approach (with the help of CodeClimate and Travis CI) allowed us to almost always keep the master branch working without any hiccups, as failing tests were never acceptable on the master branch.

Tan took on the role of Scrum Master and Project Manager. In those roles, he was responsible for ensuring that as a team, we were completing tasks at the pace necessary to complete our project and meet all deadlines. We made use of [waffle.io](https://waffle.io) to manage our Github issues, and he made sure that all our tasks and issues were always up to date.

Overall, we all embraced these collaborative guidelines we established, and feel that it contributed greatly to our success

## Conclusion

The biggest challenges and struggles we faced while working with the project were a result of the legacy code we inherited. The design decisions we made and our excellent teamwork allowed us to overcome any issues we faced, ensuring that we delivered a working and relatively polished product.

Thank you,

- [Allison](https://twitter.com/allielarson1212), Chad, [Jonmichael](https://twitter.com/tyrbo), and Tan
