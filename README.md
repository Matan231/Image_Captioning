# Image Captioning
## Overview
In image captioning the goal is to describes a given image in nutural langauge.
for exemple:
## Model architecture

**Encoder**
- pretrained Resnet50 without the last 2 fully connected layers.

**Decoder**
- Multi-head attention (4 heads) (dim(q) = dim(k) = dim(v) = 2048 
- lstm (1024+2048 -> 1024)
- fc with dropouts (p=0.25) (1024 -> vocab-size/2)
- relu 
- fc (vocab-size/2 -> vocab-size)
- enc dem = 2048
 - dec dem = 1024

**optimization:**
lr = 0.0003
Adam optimizer

## Examples


