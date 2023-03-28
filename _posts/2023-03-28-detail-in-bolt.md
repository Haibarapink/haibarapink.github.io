---
layout: post
title:  "Details in bolt db"
---
## node init
The node reads the page from the disk, and then init the node's elements from the page.
```
node on disk:
|meta data|key_size|value_size|pos|....|key|value|key|value|
```

## node Insert 
After the node's elements changes, need to call the `node.spill()` to update the node's page.

## Split timing
The bolt's split timing is when the node's page can't hold the node's elements.
node will call the `sizeLessThan` function to check the node's page can hold the node's elements.


...
