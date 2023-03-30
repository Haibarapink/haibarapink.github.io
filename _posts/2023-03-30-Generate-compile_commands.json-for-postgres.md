---
layout: post
title:  "Generate compile_commands.json for postgres"
---
# Generate compile_commands.json for postgres
compile_commands.json is a file used by clangd to provide code completion, jump definition, etc.
Postgresql is a makefile based project, I'm a C++ programmer, I'm used to use CMake to generate compile_commands.json for my project, so I want to generate compile_commands.json for postgres, I found a tool called `bear`

Get into the postgres source code directory.

In ubuntu, you can install it by 
```
sudo apt install bear 
```

In the earily version of bear, your command line should be like this:
```
bear make
```

But in the lastest version, you can use it like this:
```
bear --make
```

Then you can find compile_commands.json in the current directory.
