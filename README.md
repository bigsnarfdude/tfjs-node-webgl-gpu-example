# tfjs-node-webgl-gpu-example

Using TensorFlow.js with pre-trained MobileNet model for image classification on Node.js.


** This project is under heavy development **


This code is using **Experimental WebGL GPU version** where NVIDIA GPU is not available to speed up inference.

* Follows development of code from TFJS repo
https://github.com/tensorflow/tfjs/tree/master/tfjs-backend-nodegl

* Demo instructions here for benchmarking
https://github.com/tensorflow/tfjs/tree/master/tfjs-backend-nodegl/demo



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



# MobileNet tfjs-backend-nodegl Demo

*This is a very early demo to show how tfjs-backend-nodegl can be used for headless WebGL acceleration.*

To run this demo, perform the following:

1. Move into `tfjs-backend-nodegl` (parent directory of this demo folder):
```sh
$ cd tfjs-backend-nodegl
```

2. Build package and compile TypeScript:
```sh
$ yarn && yarn tsc
```

3. Move into the demo directory:
```sh
$ cd demo
```

4. Prep and build demo:
```sh
$ yarn
```

5. Run demo:
```sh
$ node run_mobilenet_inference.js dog.jpg
```

Expected output:
```sh
$ node run_mobilenet_inference.js dog.jpg
Platform node has already been set. Overwriting the platform with [object Object].
  - gl.VERSION: OpenGL ES 3.0 (ANGLE 2.1.0.9512a0ef062a)
  - gl.RENDERER: ANGLE (Intel Inc., Intel(R) Iris(TM) Plus Graphics 640, OpenGL 4.1 core)
  - Loading model...
  - Mobilenet load: 6450.763924002647ms
  - Coldstarting model...
  - Mobilenet cold start: 297.92842200398445ms
  - Running inference (100x) ...
  - Mobilenet inference: (100x) : 35.75772546708584ms
```

