# LeafCounting
Supporting code for paper "Leaf Count Aided Novel Framework for Rice (Oryza-Sativa L.) Genotypes Discrimination in Phenomics: Leveraging Comput-er Vision and Deep Learning Applications"

```
git clone https://github.com/pjreddie/darknet
cd darknet
```

#For printing coordinates of leaftips later, copy following files from attached directory "LeafTipDetection" i.e. :-
```
git clone https://github.com/mkvishal174314001/LeafCounting.git
cp LeafCounting/src/image.c ./src/ 
make
```

#run following to get coordinates in terminal (use "&>> log" in end to save in log) and image with leaftip boxes:-

```
./darknet detector test LeafCounting/leaftipSingle.data LeafCounting/leaftipSingle.cfg LeafCounting/leaftipSingle_56000.weights LeafCounting/testdata/229.png
```
