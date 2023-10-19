# Counterfeit_detection
An algorithm for detecting counterfeit banknotes

My goal is to build an algorithm which, based on the geometric characteristics of a banknote, would be able to determine whether it was a real or fake banknote.

## Technologies
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)


## About data

Geometric dimensions data model :

I currently have six pieces of geometric information about a banknote :

  - Length: the length of the banknote (in mm);
  - height_left: the height of the banknote (measured on the left side, in
mm);
  - height_right: the height of the banknote (measured on the right side, in mm);
  - margin_up: the margin between the top edge of the banknote and the banknote image (in mm)
(in mm)
  - margin_low: the margin between the bottom edge of the banknote and its image (in mm)
(in mm)
  - diagonal: the diagonal of the banknote (in mm)

**This is the information that the algorithm has to work with.**

Parameterisation file :
   
I have an example file containing 1,500 banknotes, which you can use as you wish to parameterise your algorithm. Of these 1,500 notes, 1,000 are true and 500 are false; a column has been added to indicate the type of note.


## The algorithm

General operation of the algorithm

I have six pieces of geometric data for each ticket. The algorithm must therefore be able to take as input a file containing the dimensions of several banknotes, and determine the type of each of them based on the dimensions alone. To this end, I have the standard format of our ticket files that the algorithm should work with in a file called billets_production.csv.

I wanted to compare two prediction methods :

  * a classic logistic regression;
  * a k-means, using the centroids to make the prediction

Obviously, this algorithm will have to perform well in order to identify as many counterfeit notes as possible from the mass of notes analysed each day.

