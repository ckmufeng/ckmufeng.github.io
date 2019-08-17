---
layout:     post
title:      Homebrew install local archive
subtitle:   
date:       2019-08-17
author:     BY ckmufeng
header-img: img/post-bg-alibaba.jpg
catalog: true
tags:
    - MacOs, brew
---

> Homebrew install local archive

# Homebrew install local archive

找了很多中文网页，都是说将下载的压缩包直接放到~/Library/Caches/Homebrew下，
但该方法并不完整，实验可行的方法如下：
```
wget source-version.tar.gz
mv source-version.tar.gz $(brew --cache -s <formula>)
```

参考链接：https://apple.stackexchange.com/questions/84403/how-to-use-homebrew-to-install-local-archive

