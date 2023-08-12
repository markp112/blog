---
layout:     post 
title:       "Git Commands"
subtitle:    ""
description: "A selection of useful git commands"
date:        2023-08-10
author:      "Mark Phillips"
URL: "/2023/08/10/git-commands/"
published: true
image:       ""
tags:        
  - Git
categories:  []
---

## Rename branch Master to Main 
```
git branch -m master main
```
make a change to the code and do a git push to origin main using

``` 
git push -u origin main
```
next delete the remote master branch
```
git push origin --delete master
```
 