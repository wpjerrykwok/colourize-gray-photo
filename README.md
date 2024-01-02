# Colourize Gray Photo
A project to colourize gray scale photo using generative adversial network (GAN)

## Motivation
This project aims to gain a better understanding of the old times captured in grayscale photographs by transforming them into visually compelling colour images. Recognizing that photos from the past were predominantly grayscale, the objective is to enhance their appeal by leveraging a generative adversarial network (GAN) for colorization.  

## What the model does
Specifically, the GAN is trained on grayscale images featuring human faces. The training process involves supplying the GAN with paired inputs, comprising a grayscale image and its corresponding colour version, with the expectation of obtaining a colourized version. 

## How I built it
The images undergo preprocessing steps such as resizing and normalization, and they are then divided into training, validation, and testing sets. Two models are implemented in this project. The first model, named *pix2pix*, utilizes a conditional GAN as its generator and a PatchGAN as its discriminator. The second model, called *noPatch*, employs a more conventional discriminator architecture from a deep convolution GAN. 

## Challenges I faced
The first challenge was to get the GAN working with the input images. The second challenge was to have resources to train the model within the timeframe to get meaningful results.

## Accomplishments
By comparing the outputs, *pix2pix* model excels in preserving the detail in the original image while giving a vivid colour palette to the grayscale input. 

## What I learned
I learn different GAN architecture. I learn using the utilities from tensorflow to plot the structure of a model. I learn how to use opencv for image input. I learn how to analyze a well-established model and modify it to suit my use case. 

## What's next for the model
Further work could be done towards implementing a two-step approach, by first detecting the contour of the face and then applying the colourization by segments. The *pix2pix* model can be applied on style transfer as well. 

## Built with
python tensorflow opencv numpy matplotlib