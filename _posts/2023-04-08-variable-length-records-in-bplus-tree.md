---
layout: post
title:  "Variable Length Records in B+ Tree"
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
Keep updating...