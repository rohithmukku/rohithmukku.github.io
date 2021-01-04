---
layout: post
title: Face Mask Detection
description: Face Mask detection using Pytorch, OpenCV
tags:
- machine learning
- python
categories:
- machine learning
---

Well I'd a lot of free time and I was trying to learn Pytorch, so I made a simple project of face mask detection. (Note: This project doesn't seem to show the best results but is decent enough.)

<!--![No Mask screenshot](/assets/face_mask_detection/example_1.jpg)-->
<div class="image-row" markdown="1">
  <div class="image-column" markdown="1">
  <figure>
  <img src="/assets/face_mask_detection/example_1.jpg" alt="No Mask screenshot" width="300"/>
  <figcaption>No Mask example
  </figcaption>
  </figure>
  </div>
  <div class="image-column" markdown="1">
  <figure>
  <img src="/assets/face_mask_detection/example_2.jpg" alt="Mask screenshot" width="300"/>
  <figcaption>Mask example
  </figcaption>
  </figure>
  </div>
</div>

As you can see, the model I trained can do a lot better at detecting masks, but nevertheless this was for learning purpose. My mask classifier model is a very simple one as shown below,
I used 3 Convolutional layers and 3 Fully Connected Layers. The dataset can be found [here](https://github.com/chandrikadeb7/Face-Mask-Detection) and the mask classifier model was
trained on 30 epochs. Test accuracy was around 98%. For face detection I used OpenCV's frontal face cascade classifier and then predicted on the detected regions.

<figure>
  <img src="/assets/face_mask_detection/model_summary.jpg" alt="Model Summary" width="500"/>
  <figcaption> Model Architecture
  </figcaption>
</figure>

### Improvements/Future Work
- The model can be trained further on more data, also the model architecture can be more complex.
- Use Streamlit for interactive experience.

### References
- <https://www.pyimagesearch.com/2020/05/04/covid-19-face-mask-detector-with-opencv-keras-tensorflow-and-deep-learning/>
- <https://towardsdatascience.com/real-time-face-recognition-an-end-to-end-project-b738bb0f7348>
- <https://machinelearningmastery.com/how-to-perform-face-detection-with-classical-and-deep-learning-methods-in-python-with-keras/>
- [Dataset](https://drive.google.com/drive/folders/1XDte2DL2Mf_hw4NsmGst7QtYoU7sMBVG)
