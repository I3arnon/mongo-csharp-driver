+++
date = "2015-03-17T15:36:56Z"
draft = false
title = "Upgrading"
[menu.main]
  parent = "What's New"
  identifier = "Upgrading"
  weight = 10
  pre = "<i class='fa'></i>"
+++

## Breaking Changes

### Backwards compatibility with driver version 2.7.0–2.13.x

Driver version 2.14.0 only supports MongoDB 3.6 and later. It cannot connect to
clusters running earlier versions of MongoDB. If you need to connect to
an older cluster, please use driver version 2.13.x or earlier.

Starting in 2.11.0, ``BsonSerializer.Serialize`` will throw an
``InvalidOperationException`` when attempting to serialize an array at
the root of a BSON document. Prior versions would allow this invalid operation.
See https://jira.mongodb.org/browse/CSHARP-2877 and
https://jira.mongodb.org/browse/CSHARP-3889 for more details.
