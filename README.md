# Image-Caption-Generator
Generate caption for a given image - Personal learning

## Introduction
Image caption generator is a Deep Learning based model designed to generate a textual description of an image. It uses computer vision techniques to extract features from the image and natural language processing to generate a textual description. 

## Data
Flickr8k is a good starting dataset as it is small in size and can be trained easily on low-end laptops/desktops using a CPU.

## Approach

he encoded image and text caption, and the decoder makes predictions based on the output. Our model utilizes a CNN as the "image model" and an RNN/LSTM as the "language model" to encode text sequences of varying length. The vectors from both encodings are then merged and processed by a Dense layer for the final prediction.

For encoding the image features, we will employ transfer learning, using models such as VGG-16, InceptionV3, or ResNet. To encode the text sequence, we will map each word to a 200-dimensional vector using an embedding layer, and we will compare the results using a pre-trained Glove model.

To generate the caption, we will employ two popular methods, Greedy Search and Beam Search, to select the best words to describe the image accurately.

## Improvements
Things you can implement to improve your model:

- Make use of the larger datasets, especially the MS COCO dataset or the Stock3M dataset which is 26 times larger than MS COCO.
- Implementing an Attention Based model:- Attention-based mechanisms are becoming increasingly popular in deep learning because they can dynamically focus on the various parts of the input image while the output sequences are being produced.
