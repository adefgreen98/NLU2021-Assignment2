# NLU2021-Assignment2

In this assignment we are required to test the SpaCy parser using the CoNLL 2003 dataset as ground-truth for comparison.

### Directory structure
For the execution of this project it is *highly recommended* to use Google Colab. If that is not the case, here are the instructions for
the required directory structure.

If the .ipynb is not modified, it automatically downloads this repo and creates the correct arrangement of directories needed for execution. 

Otherwise, if both the git-request cell and the copy cell (to put `conll.py` in parent directory) are deactivated, the program expects to find the following directory structure: 
```
<parent>
  |_Assignment2.ipynb
  |_conll.py
  |_NLU2021-Assignment2/
      |_ [...]
      |_data/
          |_conll2003.zip
```
Note that in this case it will **extract the .zip** file automatically. If this is not desired, then also a directory named `data` should be included at the parent directory level, with inside the `test.txt` test set:
```
<parent>
  |_Assignment2.ipynb
  |_conll.py
  |_data/
      |_ [...]
      |_test.txt
```

### Requirements

+ SpaCy: the .ipynb file has been tested with versions 2.4.4 and 3.0.3; it should work independently from the version, however results
may be different, due to some changes in newer version's entity tagger;
+ [Seaborn](https://seaborn.pydata.org/): to visualize frequency counts of entity tags;
+ Pandas: to visualize tables from the CoNLL evaluation funciton (included in conll.py);
+ Sklearn: for classification metrics.

Moreover, the .ipynb file requires the presence of `conll.py` inside the same folder, so that it can import the `evaluate()` function for Exercises 2 & 3.

**Note on Seaborn**: to have a better view of Exercise 2 results, an histogram is plot using Seaborn library. This is best viewed in Jupyter or Google Colaboratory, and so 
it has not been tested for local execution; it should not cause any issue (other than missing the histogram plot).

### Execution time
Due uniquely to SpaCy parsing method, which takes the great majority of execution time, a single run of this project requires around **1.30 - 2 minutes** to be completed. 
