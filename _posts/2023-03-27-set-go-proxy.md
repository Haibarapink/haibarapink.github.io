---
layout: post
title:  "Install Go-Tools on Windows in China"
---

Because of the GFW, we can't use `go get` to install Go-Tools in China. So we need to set a proxy for `go get`.
Here are the steps:

Set the proxy 'goproxy.cn' in the environment variable `GOPROXY`.

After that you can use `go get` to install Go-Tools.

You can set GOPROXY by command line like this:

```bash
set GOPROXY=https://goproxy.cn,direct
```
Or you can set GOPROXY in the environment variable `GOPROXY` in Windows.