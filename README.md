# Flipping page detector
## Background:
Our company develops innovative Artificial Intelligence and Computer Vision solutions that revolutionize industries. Machines that can see: We pack our solutions in small yet intelligent devices that can be easily integrated to your existing data flow. Computer vision for everyone: Our devices can recognize faces, estimate age and gender, classify clothing types and colors, identify everyday objects and detect motion. Technical consultancy: We help you identify use cases of artificial intelligence and computer vision in your industry. Artificial intelligence is the technology of today, not the future.

MonReader is a new mobile document digitization experience for the blind, for researchers and for everyone else in need for fully automatic, highly fast and high-quality document scanning in bulk. It is composed of a mobile app and all the user needs to do is flip pages and everything is handled by MonReader: it detects page flips from low-resolution camera preview and takes a high-resolution picture of the document, recognizing its corners and crops it accordingly, and it dewarps the cropped document to obtain a bird's eye view, sharpens the contrast between the text and the background and finally recognizes the text with formatting kept intact, being further corrected by MonReader's ML powered redactor.

MonReader is a new mobile document digitalization experience for the blind, for researchers and for everyone else in need for fully automatic, highly fast and high-quality document scanning in bulk. It is composed of a mobile app and all the user needs to do is flip pages and everything is handled by MonReader: it detects page flips from low-resolution camera preview and takes a high-resolution picture of the document, recognizing its corners and crops it accordingly, and it dewarps the cropped document to obtain a bird's eye view, sharpens the contrast between the text and the background and finally recognizes the text with formatting kept intact, being further corrected by MonReader's ML powered redactor.

## Data Description:
We collected page flipping video from smart phones and labelled them as flipping and not flipping. We clipped the videos as short videos and labelled them as flipping or not flipping. The extracted frames are then saved to disk in a sequential order with the following naming structure: VideoID_FrameNumber

## Goal(s):
1) Predict if the page is being flipped using a single image.
2) Predict if a given sequence of images contains an action of flipping.

## Methodology:
The images extracted from the videos are pre-processed in order to maximize the performance of the model used. The pre-processing consists in: cropping the images to exclude not informative areas, resizing the images to be compatible with the model input and normalizing the images. The model used is a pre-trained convolutional network called MobileNet-v2 which it is fine-tuned used the data availiable. The fine-tuning of few parameters maximises the performance of the model with limited data. The model detecting the flipping images was then used to classify videos containing a flipping action. The flipping action is present in a video when one of more images in the sequence is classified as flipped.

## Conclusions:
The flipping page detector model achieves an F1 score of 0.96 classifying 296 true positive samples, 11 false negative samples, 275 true negative samples and 15 false positive samples. The goal of the project is achieved and after an examination of the misclassified examples it is clear that they are all borderline which make them difficult to classify. 
