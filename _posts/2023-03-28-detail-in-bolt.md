---
layout: post
title:  "Details in bolt db"
---

## node Insert 
The bolt's nodes copy is deep copy.
After the node's elements changes, need to call the `node.spill()` to update the node's page.

## Split timing
The bolt's split timing is when the node's page can't hold the node's elements.
node will call the `sizeLessThan` function to check the node's page can hold the node's elements.


...
