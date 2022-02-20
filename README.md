# Image Captioning
## Overview
In image captioning the goal is to describes a given image in nutural langauge.

The model is traind on Flickr8k Dataset from [here](https://www.kaggle.com/adityajn105/flickr8k/activity)
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

![alt text](https://github.com/Matan231/Image_Captioning/blob/main/examples/image1PNG.PNG)

![alt text](https://github.com/Matan231/Image_Captioning/blob/main/examples/image2PNG.PNG)

![alt text](https://github.com/Matan231/Image_Captioning/blob/main/examples/image3PNG.PNG)

### failing exemple

![alt text](https://github.com/Matan231/Image_Captioning/blob/main/examples/image_failing_example.PNG)
