# U-Net based model for detecting landslides
This project utilizes the U-Net architecture for detecting landslides in satellite images. The U-Net model is trained with a custom loss function and evaluated using the Jaccard coefficient as a metric. 
The goal is to accurately identify landslide-affected areas in satellite imagery.
## Dependencies and software versions required to run the project. 
1. Python
2. Tensorflow
3. Numpy
4. Matplotlib
5. Opencv
## Data
Data for this project was taken from IARAI, Institute of Advanced Research in Artifical Intelligence.
All bands in the competition dataset are resized to the resolution of ~10m per pixel. The image patches have the size of 128 x 128 pixels and are labeled pixel-wise.
# Unet Architecture
Here's a brief overview of the U-Net architecture:

### Contracting Path (Encoder):
The top part of the U, often referred to as the encoder, consists of a series of convolutional and pooling layers.
Convolutional layers with small receptive fields are used to capture local features.
Max pooling operations are applied to reduce spatial dimensions and increase the receptive field.

### Bottleneck:
At the bottom of the U, there is a bottleneck layer that captures the most essential information from the input image.
It typically involves several convolutional layers without pooling.

### Expansive Path (Decoder):
The bottom part of the U, known as the decoder, involves upsampling and concatenation operations to recover the spatial resolution.
Convolutional layers with larger receptive fields are used to capture global features.
Transposed convolutions (also known as deconvolutions or upsampling) are used to increase spatial dimensions.

### Skip Connections:
The key innovation of U-Net is the use of skip connections, where feature maps from the contracting path are concatenated with feature maps in the expansive path.
This helps to retain high-resolution information and aids in the precise localization of segmented objects.





