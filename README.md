# Latent Space Visualization
Visualize the Latent Space of an Autoencoder using matplotlib

## What’s the Latent Space ?

An Autoencoder is made of two components: an Encoder & a Decoder. The Encoder brings the input data from a high dimensional representation to a bottleneck layer, where the number of neurons is the smallest. Then, the decoder takes this Encoded Input and converts it back to the original Input shape. The latent space is the space in which the data lies in the bottleneck layer.

<p align="center">
<img src="https://github.com/crypto-code/Latent-Space-Visualization/blob/master/assets/model.png" width="900" height="400" align="middle" />   </p>

The Latent Space contains a compressed representation of the image, which is the only information the decoder is allowed to use to try to reconstruct the input as fully as possible. To perform well, the network has to learn to extract the most relevant features in the bottleneck.

Once the Latent Space is plotted on a 2D space images can be generated by sampling from any point in that space.

## Requirements:
* Python 3.6.2 (https://www.python.org/downloads/release/python-362/)
* Numpy (https://pypi.org/project/numpy/)
* Tensorflow (https://pypi.org/project/tensorflow/)
* Keras (https://pypi.org/project/Keras/)
* Matplotlib (https://pypi.org/project/matplotlib/)
* Pillow (https://pypi.org/project/Pillow/)
* OpenCV (https://pypi.org/project/opencv-python/)

## Usage:

* Firstly, collect the required dataset of images to visualize (A datset of pokemon sprites is already provided). Once collected, the images need to be converted to RGB and then resized to 64x64 to fit the Autoencoder using RGBA2RGB.py & resize.py.
```
python RGBA2RGB.py --help

usage: RGBA2RGB.py [-h] --input INPUT --output OUTPUT

Convert RGBA to RGB

optional arguments:
  -h, --help       show this help message and exit
  --input INPUT    Directory containing images to resize. eg: ./resized
  --output OUTPUT  Directory to save resized images. eg: ./RGB_data
```

```
python resize.py --help

usage: resize.py [-h] --input INPUT --output OUTPUT

Resize Input Images

optional arguments:
  -h, --help       show this help message and exit
  --input INPUT    Directory containing images to resize. eg: ./data
  --output OUTPUT  Directory to save resized images. eg: ./resized
```

* Once the dataset is prepared, run LS_visualize in training mode to train the autoencoder.
```
python LS_visualize.py --help
usage: LS_visualize.py [-h] --input INPUT --name NAME [--epoch EPOCH] --mode MODE

Autoencoder Latent Space Visualization

optional arguments:
  -h, --help     show this help message and exit
  --input INPUT  Directory containing images eg: data/
  --name NAME    Model Name
  --epoch EPOCH  No of training iterations
  --mode MODE    Mode: train or plot
```
Once trained the latent space can be plotted by setting the mode to plot.

## Example:
<p align="center">
<img src="https://github.com/crypto-code/Latent-Space-Visualization/blob/master/assets/example.gif" height="400" align="middle" />   </p>
Hovering over any region in the 2D space gives a reconstructed image. Images at points give perfect reconstruction, while in the white space a mix of different images is visible.

# G00D LUCK

For doubts email me at:
atinsaki@gmail.com
