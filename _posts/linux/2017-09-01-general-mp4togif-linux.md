---
layout: post
title: linux下用ffmpeg实现mp4转gif格式
category: Linux
tags: linux
description: linux下用ffmpeg实现mp4转gif格式
---

首先，有一个网站可以免费在线转换格式：https://ezgif.com/video-to-gif

### 安装ffmpeg
```bash
sudo apt-get install ffmpeg
```
使用ffmpeg命令进行格式转换:
```bash
ffmpeg -i target.mp4 -s 320x240 target.gif
```
还可以添加更多参数
```bash
ffmpeg -t 4 -ss 00:00:01 -i target.mp4 -s 320x240 target.gif
```

- -i 进行格式转换
- -s 目标尺寸，与原视频尺寸无关，可以任意设置，只要你喜欢
- -t gif的时长
- -ss 其实时间，相对原视频而言