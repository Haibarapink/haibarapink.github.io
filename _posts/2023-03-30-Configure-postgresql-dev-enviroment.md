---
layout: post
title:  "Configure postgresql development enviroment!"
---
Linux enviroment:
I am a C/C++ programmer. The most popular LSP in C++ is clangd, which can make code completation,
code jump, and so on.Usually I configure a c++ project by cmake like this : `CMAKE_EXPORT_COMPLIE_COMMANDS=1`, but the postgresql is a makefile project. I can't export a compile_commands.json file.

We need `bear`, In ubuntu :
```
sudo apt install bear
```
Then in the project dir run:
```
bear make
```
The compile_commands.json is export!

