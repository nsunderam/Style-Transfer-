# Style-Transfer-
An implementation of Image Style Transfer Using Convolutional Neural Networks, by Gatys 
Given one content image and one style image, we aim to create a new, target image which should contain our desired content and style components.

The following content image will be used:

![5](https://user-images.githubusercontent.com/39443902/58421881-0e483980-8089-11e9-9c56-a95ddf03e896.jpg)


The following style image will be used:


![Van_Gogh_-_Terrasse_des_Cafés_an_der_Place_du_Forum_in_Arles_am_Abend1](https://user-images.githubusercontent.com/39443902/58422455-8400d500-808a-11e9-8beb-806f65931822.jpeg)


We will use a pre-trained VGG19 Net to extract content or style features from a passed in image.

VGG19 is split into two portions:

vgg19.features, which are all the convolutional and pooling layers
vgg19.classifier, which are the three linear, classifier layers at the end

To get the content and style representations of an image, we have to pass an image forward through the VGG19 network until we get to the desired layer(s) and then get the output from that layer.
