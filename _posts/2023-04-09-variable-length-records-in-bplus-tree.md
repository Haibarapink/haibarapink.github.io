---
layout: post
title:  "Variable Length Records in B+ Tree"
---
# Insertation in B+ Tree
The insertation in bplus-tree following the steps below:
1. Find the leaf page to insert the record.
2. Insert the record into the leaf page.
3. Check the size of the page.If the size is larger than PAGE_SIZE, split the page, set the parents of new node . else return.
4. The node is split into two nodes: leaf and right.If node's type is InternalNode, change the parents of the children which split into the the new node. Then insert the right node into the parent node, and the key is the first key of the right node.
5. Repeat step 3 and 4 until the root node is not split.If the root node is split, create a new root node, and the insert the left and right node into the new root node, update the root node pointer.
---
# Deletation in B+ Tree
The deletation in bplus-tree following the steps below:
1. Find the leaf page to delete the record.
2. Delete the record from the leaf page.
3. Check the size of page and the number of keys, if the size is smaller than PAGE_SIZE/4 and the number of keys is larger than min_keys(leaf is 1, internal is 2), get into step 4. else return.
4. Find the brother, and if the size of brother sum with the size of the node is larger than PAGE_SIZE, get into step 5. else get into step 6.
5. Fetch the first or last key from brother(if brother node is left, fetch the last key, else fetch the first key), and insert the key into the node, and delete the key from the brother node.
6. Put the right node's keys & values into left node, and delete the right node from the parent node.
7. Follow step 3 and 4 until the root node is not merged.If the root node is merged, update the root node pointer. 
---
# Variable Length Records in B+ Tree
The standard design for variable-length records in fixed-length pages in bplus-tree, 
employs an indirection vector for the records. 

Here is the example of the disk page in a database.

item : |key_pos|key_size|

records : |bytes|

page : |item1|item2|item3|item4|....|records1|records2|records3|records4|....|

---
# How to update a page in variable-length bplus-tree?
Find the page, and read the page into memory. And deserialize the page to a data structure. Then 
modify the data structure. Finally, serialize the data structure to a page, and write the page.
---
# Normailzed Keys
Records are saved as a sequence of bytes, and compared by the methods , such as memcmp. 
This way reduces the cost of comparisions, and many implementations of bplus-tree use this way.
---