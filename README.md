# iMPT-FDNPL
Function: Identification of membrane protein types is an essential problem in cells biology. The iMPT-FDNPL is a powerful multi-label classifier, which can assign multiple types to given proteins. The proteins are represented by features derived from their functional domain information via a natural language processing approach, word2vector. RAndom k-labELsets with random forest as the base classifier adopted such features to construct iMPT-FDNPL. The ten-fold cross-validation results indicate that accuracy and exact matching 0.853 and 0.851, respectively. Such classifier is superior to other classifiers using features derived from different properties of proteins via various methods.

![111](https://user-images.githubusercontent.com/30385256/129306923-13750d1c-3fb1-48d5-8eac-287844409b65.png)

# Meka command
Suppose the Meka installation root directory is "E:\meka1.9.2".

1. Ten-fold cross-validaion command for Meka:
 
cd E:\meka1.9.2

E:\meka1.9.2> java -cp "./lib/*" meka.classifiers.multilabel.RAkEL -M 10 -k 5 -P 0 -N 0 -S 0 -verbosity 5 -t data\data_350.arff -x 10 -W weka.classifiers.trees.RandomForest -- -P 100 -I 100 -num-slots 1 -K 0 -M 1.0 -V 0.001 -S 1 > D:\result_350\Rakel_ranforest_k5_i100.txt


# Other requirements

The codebase is implemented in Python 3.5.6. 

   Matlab 2016a
   
   Meka 1.9.2              download address: http://meka.sourceforge.net/
   
   Word2vector             download address: https://github.com/RaRe-Technologies/gensim
