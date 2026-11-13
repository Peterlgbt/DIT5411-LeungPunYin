# DIT5411-LeungPunYin
DIT5411 Assignment

The aim of this project is to use Python with Tensorflow to recognize 13,065 different Chinese characters. Each characters have 50 samples, separate it to 2 part, 40 for training and 10 for testing. Moreover, 40 samples will become 200 samples for each character by doing translation, rotation, scaling and smoothing. 13,065 characters with 200 samples each, it is a very big dataset. So I resize the photo size from 300x300 to 64x64 and change the color images to grayscale, these can decrease the memory consumption by over 98%.

About the model, I train 3 CNN models. The first model is a 3 layers single Conv2D with 8 epochs model. The original model have only 6 epochs, but at epochs 6/6, the val_loss suddenly increase from 2.01 to 12.81. So I add 2 more epochs to train it to become normal. The second model is a 2 layers single Conv2D with 6 epochs model. As expected, it have the lowest accuracy in three model. The third model is a 3 layers double Conv2D with 6 epochs model. The original model have 1024 batch size and convolutional layer with 64 -> 128 -> 256 feature maps, but the system ran out of memory during training. So I have to decrease it to 512 batch size and convolutional layer with 32 -> 64 -> 128 feature maps.
The accuarcy of first model(3 layers single Conv2D with 8 epochs) is 78.03%
The accuarcy of second model(2 layers single Conv2D with 6 epochs) is 76.24%
The accuarcy of third model(3 layers double Conv2D with 6 epochs) is 94.05%

<img width="188" height="26" alt="image" src="https://github.com/user-attachments/assets/e8fcb74b-9bfb-457c-900d-4281287eafe9" />

<img width="292" height="23" alt="image" src="https://github.com/user-attachments/assets/342827ef-d62b-4131-a880-16a53315bad9" />

<img width="285" height="24" alt="image" src="https://github.com/user-attachments/assets/9ebd6bb9-84c6-434a-8ea1-10d77ab6ebd7" />

Reference

https://github.com/AI-FREE-Team/Traditional-Chinese-Handwriting-Dataset

https://github.com/kimanalytics/Handwritten-Digit-Recognition-using-Keras-and-TensorFlow

https://colab.research.google.com/drive/1ZWck46dROBmOHTOKf7R20Vj_TpJoIIVN?usp=sharing

https://github.com/darshitajain/Introduction-to-OpenCV
