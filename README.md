# NLP-domain-_NRAKEL
Function: NLP (domain) multi-tag identification of membrane protein types. According to the data set S1 in UniProt database (release 2012_09) and protein2ipr.txt in InterPro database, the IPR word vector corresponding to the protein is obtained. , The random k-label set (RAKEL) algorithm is used to construct a multi-label classifier, and the random forest is used as the basic algorithm. Construct a multi-label classifier NLP (domain)-NRAKEL. Through strict ten-fold cross-validation, the accuracy and exact matching degree of the classifier are both higher than 0.85. It greatly proves the superiority of our model and improves the accuracy of membrane protein identification. 

![111](https://user-images.githubusercontent.com/30385256/126054403-c7c60b6e-8f58-4c01-8325-0805df0eecdc.png)

# Meka command
Suppose the Meka installation root directory is "E:\meka1.9.2".

1. Ten-fold cross-validaion command for Meka:
cd E:\meka1.9.2
E:\meka1.9.2> java -cp "./lib/*" meka.classifiers.multilabel.RAkEL -M 10 -k 5 -P 0 -N 0 -S 0 -verbosity 5 -t data\data_350.arff -x 10 -W weka.classifiers.trees.RandomForest -- -P 100 -I 100 -num-slots 1 -K 0 -M 1.0 -V 0.001 -S 1 > D:\result_350\Rakel_ranforest_k5_i100.txt


# Other requirements

The codebase is implemented in Python 3.5.6. Information of used packages is listed below.

   Matlab 2016a
   Meka 1.9.2              download address: http://meka.sourceforge.net/
   
   Mashup                  download address: http://mashup.csail.mit.edu
