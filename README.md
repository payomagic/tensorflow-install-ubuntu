# tensorflow-install-ubuntu
How to install tensorflow on Ubuntu server

## Steps to install TensorFlow on an Ubuntu-based server: ##

Open a terminal window and update the package list using the following command:

```
sudo apt update
```

Install the required dependencies for TensorFlow using the following command:

```
sudo apt install python3-dev python3-pip libhdf5-dev libc-ares-dev libeigen3-dev \
libatlas-base-dev libopenblas-dev libblas-dev liblapack-dev cython3 \
libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev \
libx264-dev libgtk-3-dev libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev \
gfortran openexr libgstreamer-plugins-base1.0-dev libgstreamer1.0-dev
```

Install TensorFlow using pip3 with CPU support:

```
pip3 install --upgrade pip
pip3 install --user tensorflow
```

Note that the --user flag installs TensorFlow in the user's home directory rather than system-wide.

Verify the installation by running a TensorFlow test script:

```
python3 -c "import tensorflow as tf; print(tf.reduce_sum(tf.random.normal([1000, 1000])))" 
```

This script will generate a 1000x1000 matrix of random numbers and calculate the sum of all elements. If TensorFlow is installed correctly, the script will output the sum.

That's it! TensorFlow should now be installed on your server.
