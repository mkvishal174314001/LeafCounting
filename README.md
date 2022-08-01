# LeafCounting
Supporting code for paper "Leaf Count Aided Novel Framework for Rice (Oryza-Sativa L.) Genotypes Discrimination in Phenomics: Leveraging Comput-er Vision and Deep Learning Applications"

```git clone https://github.com/pjreddie/darknet
cd darknet
```

#For printing coordinates of leaftips later, copy following files from attached directory "LeafTipDetection" i.e. :-
```
git clone 
cp LeafTipDetection/image.c ./src/ 
make
```

#copy following files from attached directory "LeafTipDetection" i.e. :-
cp LeafTipDetection/leaftipSingle* .
cp -r LeafTipDetection/testdata/ .
cp LeafTipDetection/*Single.txt .
cp LeafTipDetection/leaftipSingle_10000.weights .

#run following to get coordinates in terminal (use "&>> log" in end to save in log) and image with leaftip boxes:-

./darknet detector test leaftipSingle.data leaftipSingle.cfg leaftipSingle_10000.weights testdata/229.png
