# Latent Space Visualization
Visualize the Latent Space of an Autoencoder using matplotlib

## What’s the Latent Space ?

An Autoencoder is made of two components: an Encoder & a Decoder. The Encoder brings the input data from a high dimensional representation to a bottleneck layer, where the number of neurons is the smallest. Then, the decoder takes this Encoded Input and converts it back to the original Input shape. The latent space is the space in which the data lies in the bottleneck layer.

<p align="center">
<img src="https://github.com/crypto-code/Latent-Space-Visualization/blob/master/assets/model.png" width="900" height="400" align="middle" />   </p>

The Latent Space contains a compressed representation of the image, which is the only information the decoder is allowed to use to try to reconstruct the input as fully as possible. To perform well, the network has to learn to extract the most relevant features in the bottleneck.
