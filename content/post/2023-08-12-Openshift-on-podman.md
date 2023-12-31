---
layout:     post 
title:       "OpenShift on Podman"
subtitle:    ""
description: "Various Commands and Troubleshooting resolutions"
date:        2023-08-10
author:      "Mark Phillips"
URL: "/2023/08/12/Openshift-on-podman/"
image: "/img/tree-in-snow.jpg"
published: true
image:       ""
tags:        
  - OpenShift
categories:  []
---

## Troubleshooting

### The node was low on resource: ephemeral-storage

This issue can occur due to the space available for the cache becoming full, to check this run:
```
crc status
```

Which will show something similar to the below on Windows:
```
CRC VM:          Running
OpenShift:       Running (v4.13.6)
RAM Usage:       8.107GB of 9.374GB
Disk Usage:      27.29GB of 32.68GB (Inside the CRC VM)
Cache Usage:     22.7GB
Cache Directory: C:\Users\<user>\.crc\cache

```

To make more space available to the cache the following needs to be run:
```
crc stop
crc config set disk-size 50
crc start
```

In the example above the disk is increased from the 22.7GB to 50GB
