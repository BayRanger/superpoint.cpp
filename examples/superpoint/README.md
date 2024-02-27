This example shows how to implement Superpoint point extraction and description with ggml using pretrained model weights.

If you want to integrate superpoint to your project and refuse to use thirdparty libs like libtorch, tensorrt, etc, superpoint.cpp is an option!

# Superpoint.cpp

TODO:

* image has to been preprocessed to size of 480,640
* image loading is complex and dirty

Download the model weights:

```bash
$ wget https://github.com/magicleap/SuperPointPretrainedNetwork/blob/master/superpoint_v1.pth

```

compile the project and generate the executable file

```bash
$ mkdir build
$ cd build
$ cmake ..
$ make
$ mv bin/superpoint ../examples/superpoint

```

Convert the weights to GGUF format:

```bash
$ ./convert-yolov3-tiny.py yolov3-tiny.weights
yolov3-tiny.weights converted to yolov3-tiny.gguf
```

inference

```bash
$ ./superpoint -i dog_color.jpg
```

# Reference

https://github.com/magicleap/SuperPointPretrainedNetwork
https://github.com/adityamwagh/SuperSLAM
