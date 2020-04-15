---
layout: post
title: Image Caption using Pytorch
tags: [personal project, Computer Vision]
image: /img/captioning/pred0.png
---

# Face-Landmark-Extraction-Pytorch
#### Trained with NVIDIA P100 GPU

#### Data
- COCO Dataset is used, check thier website for details [Link](http://cocodataset.org/#download)
- Training and Test data look like this:
<img src="/img/captioning/test_img.png" width="350" height="250"/> 

#### Training
- Transfer Learning is used with Resnet150 for extracting image features(Convolutional Neural Network) and Recurrent Neural Network using LSTM is used.
<img src="/img/captioning/loaded_model.png" width="450"/> 
- We can see that model is actually learning!  :stuck_out_tongue_winking_eye:
<img src="/img/captioning/train0.png" width="450"/>
<img src="/img/captioning/train_end.png" width="450"/> 

#### Testing
- Prediction: Looks like my model is working well :grinning:
<img src="/img/captioning/pred0.png" width="450"/>
<img src="/img/captioning/pred1.png" width="450"/> 
<img src="/img/captioning/pred2.png" width="450"/> 
<img src="/img/captioning/pred3.png" width="450"/> 
<img src="/img/captioning/pred4.png" width="450"/> 

#### Conclusion
Overall, with this project, I cannot underestimate the power of deep learning again.. 


### Github
- [Link](https://github.com/JaeLee18/Pytorch-Image-Caption)
