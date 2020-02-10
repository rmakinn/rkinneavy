---
Title: "Data Science"
bookCollapseSection: true
draft: true
---

# Data Science

## Resources

- [Data Science Glossary](http://www.datascienceglossary.org/)
- [Data Science Cheatsheets List](https://github.com/FavioVazquez/ds-cheatsheets#readme)
- [Introduction to Data Science - Steven Skiena](https://www.youtube.com/watch?v=Oqb3WSPOyv8&list=PLOtl7M3yp-DVBdLYatrltDJr56AKZ1qXo&index=2)
- [Statistics - Professor Leonard](https://www.youtube.com/playlist?list=PL5102DFDC6790F3D0)
- [Essence of Calculus - 3B1B](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
- [Khan Academy](https://www.khanacademy.org/)
- [Expii](https://www.expii.com/)
- [R for Data Science](http://r4ds.had.co.nz/introduction.html)
- [Harvard CS109: Data Science](http://cs109.github.io/2015/pages/videos.html)

https://www.fast.ai/

https://github.com/academic/awesome-datascience
https://learn-anything.xyz/data-science
https://www.kaggle.com/
https://github.com/wesm/pydata-book
https://bokeh.pydata.org/en/latest/

http://datacolada.org/toc

https://www.stateof.ai/

http://neuralnetworksanddeeplearning.com/chap1.html

https://natureofcode.com/book/introduction/

https://www.codebymath.com/index.php/welcome/challenges

https://www.youtube.com/watch?v=rIofV14c0tc

https://towardsdatascience.com/how-to-build-a-simple-song-recommender-296fcbc8c85

https://nbviewer.jupyter.org/github/gumption/Python_for_Data_Science/blob/master/Python_for_Data_Science_all.ipynb

https://callingbullshit.org/syllabus.html

https://github.com/nbro/understanding-math

https://ocw.mit.edu/resources/res-18-001-calculus-online-textbook-spring-2005/textbook/

https://mml-book.github.io/

http://greenteapress.com/wp/think-stats-2e/

https://blog.revolutionanalytics.com/

https://wattenberger.com/blog/d3

#### YouTube
- Henry AI Labs: https://www.youtube.com/channel/UCHB9VepY6kYvZjj0Bgxnpbw
- Lex Fridman: https://www.youtube.com/channel/UCSHZKyawb77ixDdsGog4iWA
- MIT Deep Learning: https://www.youtube.com/watch?v=O5xeyoRL95U&list=PLrAXtmErZgOeiKm4sgNOknGvNjby9efdf
- Deep Learning School '16 Talks: https://www.youtube.com/watch?v=zij_FTbJHsk&list=PLrAXtmErZgOfMuxkACrYnD2fTgbzk2THW
- Jeremy Howard (Fast.ai): https://www.youtube.com/user/howardjeremyp/
- Two Minute Papers: https://www.youtube.com/user/keeroyz
- Open AI: https://www.youtube.com/channel/UCXZCJLdBC09xxGZ6gcdrc6A
- Deepmind: https://www.youtube.com/channel/UCP7jMXSY2xbc3KCAE0MHQ-A
- Advanced Deep & RL Course: https://www.youtube.com/playlist?list=PLqYmG7hTraZDNJre23vqCGIVpfZ_K2RZs
- Geek’s Lesson Data Science Courses: https://www.youtube.com/playlist?list=PLmAuaUS7wSOPqoyeadmrImmEwBYYhByOY
- Skiena’s Data Science Fall '16: https://www.youtube.com/playlist?list=PLOtl7M3yp-DVBdLYatrltDJr56AKZ1qXo
- MIT Intro To Probability: https://www.youtube.com/playlist?list=PLUl4u3cNGP60hI9ATjSFgLZpbNJ7myAg6
- MIT Statistics For Applications: https://www.youtube.com/playlist?list=PLUl4u3cNGP60uVBMaoNERc6knT_MgPKS0


---

## Data Science Manual - Skiena - Notes

Preface:
Do the simple things right
Develop a foundation in mathematical thinking, and intuition in statistics and linear algebra
“Genuine rigor is impossible until after there is comprehension”
Think like a computer scientist, act like a statistician
CSers ->
algorithmic manipulation of data
use of machine learning
mastery of scale
Statters ->
domain understanding
appreciation of the small
quest for significance
hunger for exploration

Ch1: what is ds?
Classification is what is says on the tin - predict the winner of a match, decide a genre - select a label from possible choices
Regression is a forecasting of a value - the future value of a numerical function (of previous values and other relevant features)

Big data i.e. large data sets -
data size up, analysis cycle time down
difficult to viz
Simple models do not require massive data to fit or evaluate
Do not exceed the minimum order of magnitude required to solve your problem
Separate the goats from the sheep - relevance to the task at hand - the right data - is superordinately powerful

Quantitative data is easily worked with in algebraic formulas and models and nice to visualise
Mathematical techniques
Categorical (i.e. qualitative) data - classification & clustering methods to generate labels from numerical data
Philosophy: epistemology, rationality
Analytical & critical: success in generating an answer, logical implausibilities or inconsistent results
Unstructured data (collection of tweets) -> translation into matrices (row - tweet, column - word freq) -> structured data -> analysis pipeline
Data collection & cleaning precedes unstructured data - this process is most of a DS job
Much opportunity for incompetence and failure here…!

Ch2: Math prelims

“probability theory enables us to find the consequences of a given ideal world, while statistical theory enables us to measure the extent to which our world is ideal”.

Probability
An experiment is a procedure which yields outcomes which are members of a sample space S (set of possible outcomes)
An event is a particular subset of the outcomes (“in the event that two rolls add up to 7” aka the subset E = {(1,6), (2,5)} etc)
Probability of an outcome s is denoted p(s) is a number with these two properties:
For each outcome s in sample space S, s is between 0 and 1
The sum of all probabilities of all outcomes adds up to 1
The probability of an event E, is the sum of the probabilities of the outcomes of the experiment
Sometimes you measure the complement (the case where E does not occur) because that’s easier

Descriptive statistics
Correlation Analysis
Logarithms

---

## Metis Data Science Bootcamp Curriculum

[PDF](https://www.thisismetis.com/assets/files/Metis-Bootcamp-Curriculum-52f9979f4f638857bc185b0b788d6d832efb7f34d3b240e199dc6d3f2eef40ed.pdf)

Essential Skills (70-100hrs)
GitHub
Bash
Python (Intermediate-Advanced)
Linear Algebra
Statistics
Touch on:
Pandas
SQL
HTML/CSS/JS
12 Weeks: Overview (420hrs - 35/wk)
First 8
Learn theory/skills/tools through iterative project-centered skill acquisition
Three projects each training up different key aspects
Final 4
Passion project
Daily Flow
Pair programming, interactive lectures
Investigations and presentations, challenges and project work
By week
1
Data wrangling and EDA (pandas, matplotlib)
Git, branching and pull requests
Project 1
Clean data and look for patterns in something like street traffic for a theoretical client
2
Probability theory (discrete, continuous)
Hypothesis Testing
Regression & model evaluation in statsmodels & scikit-learn
Web scraping with bs4 and selenium
Iterative design/design thinking
3
Bayes
Regression models (assumptions, transformations, overfitting, train/test splits)
Cross-validation and regularisation (lasso, ridge, elastic net) for refining models
More plotting (matplotlib and seaborn)
Project 2
Use regression to predict box office gross using data collected by oneself, stored in flat files
Regularise and evaluate using statsmodels/sci-kit learn
Organise and present findings to a fictional client
4
Supervised learning
Classification algorithms - k-nearest, logistic regression, SVM, decision trees, random forest
Bias-variance tradeoff, classification errors
SQL and using cloud servers/VPS
5
More supervised learning algs - Naive Bayes, Categorical MLE, Poisson Regression, Neural Networks, Deep Learning
Machine Learning - automated feature selection, stochastic gradient descent, advanced model evaluation
Fundamentals - Binomial, Bernoulli, Poisson distributions
6
Flask/Django
JS & D3.js
Dashboard Design
(Revise previous week)
Project 3
Get pre-cleaned data into an SQL db
Use supervised learning to create a dashboard using d3.js, presenting predictions
These pull from a db API made in Flask
7
More DBs, RESTful APIs
NLP - textblob, nltk, chunking, stemming, POS tagging, tf-idf
Unsupervised learning - overview & k-means
ML topics - curse of dimensionality, dimension reduction, PCA, SVD, LSI
8
NLP - topic modeling, LDA, word2vec
Unsupervised learning - hierarchical clustering, DBSCAN, Mean Shift, Spectral
ML topics - distance metrics
Project 4
Custom:

design analysis according to fictional custy with use-case/requirements
scrape, clean and organise data into a (NoSQL) DB, accessed via a RESTful API
use NLP/unsupervised learning techniques within analysis
present findings clearly
bonus: test predictions against the real world
9-12 + Final Project
Big Data: Hadoop, Spark
MapReduce
Project mgmt: iterative design, MinViPs

---

## Goethe

https://www.wikiwand.com/en/Goethean_science

https://wn.rsarchive.org/Books/GA001/English/MP1988/GA001_index.html

http://muse.jhu.edu/article/371998

> Goethe was concerned with the narrowing specialization in science and emphasis on accumulating data in a merely mechanical manner, devoid of human values and human development. Linnaean botanic taxonomic system represented this in his day, a Systema naturae. Goethe intuited the practice of rational science promoted a narrowing and contracting interplay between humanity and Nature. For Goethe any science based only on physical-material characteristics and then only selected external traits, led to epistemic impoverishment and a reduction of human knowledge.[3]

> What was needed was increased ability to derive meaning from voluminous external data by looking at it from both external-sensory angles; and, from an internal angle where thinking, Feeling, Intuition, Imagination and Inspiration could all contribute to conclusions reached by the experimenter.


---

## Text Processing & Analysis

http://alias-i.com/lingpipe/

https://github.com/dbohdan/structured-text-tools

https://nv-adlr.github.io/MegatronLM

https://github.com/learnbyexample/Command-line-text-processing

https://monkeylearn.com/text-analysis/

https://blog.floydhub.com/gentle-introduction-to-text-summarization-in-machine-learning/

---

## Scientific ML

http://www.stochasticlifestyle.com/the-essential-tools-of-scientific-machine-learning-scientific-ml/

---

## Neural Networks

http://neuralnetworksanddeeplearning.com/chap1.html

https://norasandler.com/2017/10/20/What-is-a-Neural-Network.html

http://cs231n.github.io/

https://blog.acolyer.org/2019/08/19/robust-learning-from-untrusted-sources/

---

## Failing Grade

*89% of Introduction-to-Psychology Textbooks That Define or Explain Statistical Significance Do So Incorrectly*

#### Abstract
> Null-hypothesis significance testing (NHST) is commonly used in psychology; however, it is widely acknowledged that NHST is not well understood by either psychology professors or psychology students. In the current study, we investigated whether introduction-to-psychology textbooks accurately define and explain statistical significance. We examined 30 introductory-psychology textbooks, including the best-selling books from the United States and Canada, and found that 89% incorrectly defined or explained statistical significance. Incorrect definitions and explanations were most often consistent with the odds-against-chance fallacy. These results suggest that it is common for introduction-to-psychology students to be taught incorrect interpretations of statistical significance. We hope that our results will create awareness among authors of introductory-psychology books and provide the impetus for corrective action. To help with classroom instruction, we provide slides that correctly describe NHST and may be useful for introductory-psychology instructors.

---

## Philosophy of AI

http://approximatelycorrect.com/2018/06/05/ai-ml-ai-swirling-nomenclature-slurried-thought/

---

## Matrix Multiplication

http://matrixmultiplication.xyz/
