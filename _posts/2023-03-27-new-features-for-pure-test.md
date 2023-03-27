---
layout: post
title:  "New Features for Pure Test"
---

🎉🎉🎉 Pure Test 0.2.0 is released! 🎉🎉🎉

What's new in Pure Test 0.2.0?

We support marco that is like `PURE_TEST_EQ`...

And after the test case pass, we will print the time that the test case cost.

Better output for test case. 


Some out put example:
```
Running 5 test cases...
Running test case: lru_test...
[PASS]
Time cost: 0.000024s
Running test case: disk_test...
[PASS] 
Time cost: 0.022429s
Running test case: meta_page_test...
[PASS] 
Time cost: 0.000179s
Running test case: [] { BufferPoolTest().basic_test(); remove("test.db"); }...
[DEBUG][/home/pink/current/bpt/BufferPool.hpp:252]meta pagepage count 1free list size 0next 0prev -1
[DEBUG][/home/pink/current/bpt/BufferPool.hpp:252]meta pagepage count 5free list size 0next 0prev -1
[PASS] 
Time cost: 0.000310s
Running test case: [] { BufferPoolTest().huge_test(); remove("test_huge.db"); }...
[DEBUG][/home/pink/current/bpt/BufferPool.hpp:252]meta pagepage count 1free list size 0next 0prev -1
[DEBUG][/home/pink/current/bpt/BufferPool.hpp:252]meta pagepage count 5001free list size 0next 0prev -1
[PASS] 
Time cost: 0.230968s
All test cases passed!
```