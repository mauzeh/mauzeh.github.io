---
layout: post
title:  "Why MongoDB won't fix all your problems (yet)"
date:   2014-02-03 13:22:57
categories: mongodb
---

MongoDB has gained popularity fast, so fast that it has become the de-facto NoSQL solution for many different use cases: web back-end data storage, caching, and full-text search mechanisms.

<div class="bb-pull-right bb-border bb-gap-inside bb-gap-left">
	<img src="{{site.baseurl}}/assets/images/logo_mongodb.jpeg" alt="MongoDB" title="MongoDB" width="250" />
</div>

However, among Do-It-Yourself (DIY) teams, MongoDB is hard to implement successfully. This is not to say that MongoDB is a bad choice for your project, but only to say that you need to take this into account before making a decision about using MongoDB.

**Scalability**

To put it lightly, relational databases are not easy to scale. With *sharding*, MongoDB attempts to provide an alternative for this problem. However, sharding is often implemented wrongly:

1. A wrong shard key is chosen, which is an expensive mistake to fix.
2. Sharding is applied too late in the database scaling process. If the database is already running at or near full capacity, then it is much more difficult to move into a distributed data storage mechanism.

**Performance**

Ensuring optimal performance of the MongoDB infrastructure requires finetuning of all aspects of every layer of the application, database design (indexes), network, hard drives, and so on. A DIY development team may not have the capacity or knowledge to ensure that all these layers are designed for optimzal performance. Cloud providers that automate these decisions tend to charge amounts that are beyond most DIY team budgets.

**Availability and reliability**

Running MongoDB on the cloud can result in a significant increase in database availability and reliability. However, these require significant configuration efforts and continuous monitoring of performance. Again, a DIY development team might not be capable of performing these tasks without significantly impacting the progress of actual software development.

But of course, as with all technologies, limitations can be overcome, so let's see what the MongoDB ecosystem will do to ease the burden of these issues!