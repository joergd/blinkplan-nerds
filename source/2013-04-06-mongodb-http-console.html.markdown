---
title: MongoDB HTTP Console
date: 2013-04-06 10:15 UTC
tags:
---

We are busy developing our REST API, so that our Backbone frontend can create and update flatpan and pagination data. Most of the data is stored in MongoDB.

As part of the development process, we want to be able to see what is going on from Mongo's perspective. I couldn't find any log files or traces left behind from our calls, but eventually found this handy interface built into MongoDB.

It's called the HTTP Console. You can fire it up in your browser by adding 1000 to your port number you chose for Mongo. So our's is the default port 27017. Therefore,


<pre><code data-language="shell">
http://localhost:28017
</code></pre>


will give you a view into your server. You can see statistics, the last queries you can ran against your collections and so on.

If you start your MongoDB server with the --rest option

<pre><code data-language="shell">
mongod --rest
</code></pre>


then, you will be able to access further statistics via that HTTP interface.

According to the [documentation](http://docs.mongodb.org/ecosystem/tools/http-interfaces/#simple-rest-interface),

> The mongod process includes a simple REST interface, with no support for insert/update/remove operations, as a convenience – it is generally used for monitoring/alerting scripts or administrative tasks.