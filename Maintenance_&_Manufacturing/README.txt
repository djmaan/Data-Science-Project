
Deep learning has been proven to be superior in detecting and localizing defects using imagery data which could significantly improve the production efficiency in the manufacturing industry.
Great Example from LandingAI.
Detecting defects would help in improving the quality of manufacturing as well as in reducing the waste due to production defects.

Strategy #1 Steps: 
Freeze the trained CNN network weights from the first layers. 
Only train the newly added dense layers (with randomly initialized weights).
Strategy #2 Steps: 
Initialize the CNN network with the pre-trained weights 
Retrain the entire CNN network while setting the learning rate to be very small, this is critical to ensure that you do not aggressively change the trained weights.
Transfer learning advantages are:
Provides fast training progress, you don’t have to start from scratch using randomly initialized weights
You can use small training dataset to achieve incredible results

WHAT IS IMAGE SEGMENTATION?
The goal of image segmentation is to understand and extract information from images at the pixel-level. 
Image Segmentation can be used for object recognition and localization which offers tremendous value in many applications such as medical imaging and self-driving cars etc.
The goal of image segmentation is to train a neural network to produce pixel-wise mask of the image.
Modern image segmentation techniques are based on deep learning approach which makes use of common architectures such as CNN, FCNs (Fully Convolution Networks) and Deep Encoders-Decoders.
You will be using ResUNet architecture to solve the current task. 

RESUNET
ResUNet architecture combines UNet backbone architecture with residual blocks to overcome the vanishing gradients problems present in deep architectures.
Unet architecture is based on Fully Convolutional Networks and modified in a way that it performs well on segmentation tasks.
Resunet consists of three parts:
(1) Encoder or contracting path
(2) Bottleneck 
(3) Decoder or expansive path 
