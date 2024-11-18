# ReInspect
ReInspect is an neural network extension to Overfeat-GoogLeNet in Caffe. For the Tensorflow version,
see <a href="http://github.com/Anant-20/-Tiwari/tensorbox">TensorBox</a>.
It is designed for high performance object detection in images with heavily overlapping instances.


## Installation & Demo

    $ # install the apollocaffe pull request on caffe. see apollocaffe.com
    $ git clone http://github.com/Anant-20-Tiwari/reinspect
    $ cd reinspect
    $ make eval

Running `make eval` will download the data and start a <a href="https://github.com/Anant-20-Tiwari/ReInspect/blob/master/evaluation_reinspect.ipynb" target="_blank">notebook</a>
to visualize the performance of the model. If you want to train the model from scratch, you can use

    $ make train


## Running on your own data

The easiest way to run on your own data is to resize your images to 480x640 and provide labels for each object in each image with the idl text files.

Once you have verified that you can train on 480x640 images, you can also modify the image width and height options in config.json. We recommend you choose an image size which is an integer multiple of 32, and then modify the (15, 20) grid to (image_height / 32, image_width / 32).
