# LeafCounting
Supporting code for paper "Leaf Count Aided Novel Framework for Rice (Oryza-Sativa L.) Genotypes Discrimination in Phenomics: Leveraging Comput-er Vision and Deep Learning Applications"

Tested on Ubuntu 20.04

## Inference
```
git clone https://github.com/pjreddie/darknet
cd darknet
```

For printing coordinates of leaftips later, copy following files from this repo to darknet code :-
```
git clone https://github.com/mkvishal174314001/LeafCounting.git
cp LeafCounting/src/image.c ./src/ 
make
```

Run following commands to get coordinates in terminal (use "&>> log" in end to save in log) and image with leaftip boxes:-

```
./darknet detector test LeafCounting/leaftipSingle.data LeafCounting/leaftipSingle.cfg LeafCounting/leaftipSingle_56000.weights LeafCounting/testdata/229.png
```
## Feature Visualization

It is preferable to build yolo with opencv for interactive visualization. Following commands can help get visualization of weights as jpg files shown in LeafCounting/feature-viz/
```
cp LeafCounting/src/convolutional_layer.c ./src/
cp LeafCounting/src/image_opencv.cpp ./src/
cp LeafCounting/examples/darnet.c ./examples/darnet.c
make
./darknet visualize LeafCounting/leaftipSingle.cfg LeafCounting/leaftipSingle_56000.weights
```
