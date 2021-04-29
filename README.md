# NLU2021-Assignment2

In this assignment we are required to test the SpaCy parser using the CoNLL 2003 dataset as ground-truth for comparison.

### Directory structure
For the execution of this project it is *highly recommended* to use Google Colab. If that is not the case, then these are the instructions for
the required directory structure.

If the .ipynb is not changed, it automatically downloads this repo and creates the correct arrangement of directories needed for execution. 

Otherwise, if the cell containing git request is deactivated, then the required directory structure is the following one: 
```
<parent>
  |_Assignment2.ipynb
  |_conll.py
  |_NLU2021-Assignment2/
      |_ [...]
      |_data/
          |_conll2003.zip
```
In this case, it will extract the .zip file automatically; if this is not desired, then also a directory named `data` should be included at the parent directory level, like this:
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

### Execution time
Due uniquely to SpaCy parsing method, which takes the great majority of execution time, a single run of this project requires around **1.30 - 2 minutes** to be completed. 
