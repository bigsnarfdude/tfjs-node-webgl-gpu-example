# tfjs-node-webgl-gpu-example

# tfjs-node-example

Using TensorFlow.js with pre-trained MobileNet model for image classification on Node.js.
This code is using **Expermintal WebGL GPU version** where NVIDIA GPU is not available to speed up inference.


Tested:
1. Ubuntu 18.04 Intel
2. Ubuntu 18.04 Jetson TX2
3. Ubuntu 18.04 Jetson Nano
4. Raspbian Raspberry Pi4


## Step 1: Install node and npm

## Step 2: git clone this repo with

`git clone  https://github.com/bigsnarfdude/tfjs-node-webgl-gpu-example.git`

## Step 3: install dependancies

`npm install`

## Step 4: run prediction on panda.jpg against pre-trained model

`node script.js mobilenet/model.json panda.jpg`


## Expected output

`classification results: [ { className:`

`     'giant panda, panda, panda bear, coon bear, Ailuropoda melanoleuca',`

`    probability: 0.9993536472320557 },`

`  { className:`

`     'American Staffordshire terrier, Staffordshire terrier, American pit bull terrier, pit bull terrier',`

`    probability: 0.00012968324881512672 },`

`  { className: 'Arctic fox, white fox, Alopex lagopus',`

`    probability: 0.00008463481208309531 } ]`
