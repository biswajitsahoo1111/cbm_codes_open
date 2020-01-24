Condition based maintenance is the process of doing maintenance only when it is required. Adoption of this maintenance strategy leads to significant monetary gains as it precludes periodic maintenance and reduces unplanned downtime. Another term commonly used for condition based maintenance is predictive maintenance. As the name suggests, in this method we predict in advance when to perform maintenance. Maintenance is required, if fault has already occurred or is imminent. This leads us to the problem of fault diagnosis and prognosis.

In fault diagnosis, fault has already occurred and our aim is to find what type of fault is there and what is its severity. In fault prognosis, our aim is to predict the time of occurrence of fault in future, given its present state. These two problem are central to condition based maintenance. There are many methods to solve these problems. These methods can be broadly divided into two groups:

  - Model Based Approaches
  - Data-Driven Approaches

In model based approach, a complete model of the system is formulated and it is then used for fault diagnosis and prognosis. But this method has several limitations. Firstly, it is a difficult task to accurately model a system. Modelling becomes even more challenging with variations in working conditions. Secondly, we have to formulate different models for different tasks. For example, to diagnose bearing fault and gear fault, we have to formulate two different models. Data-driven methods provide a convenient alternative to these problems.

In data-driven approach, we use operational data of the machine to design algorithms that are then used for fault diagnosis and prognosis. The operational data may be vibration data, thermal imaging data, acoustic emission data, or something else. These techniques are robust to environmental variations. Accuracy obtained by data-driven methods is also at par and sometimes even better than accuracy obtained by model based approaches. Due to these reasons data-driven methods are becoming increasingly popular at diagnosis and prognosis tasks.

## Aim of the project

In this project we will apply some of the standard machine learning techniques to publicly available data sets and show their results with code. There are not many publicly available data sets in machinery condition monitoring. So we will manage with those that are publicly available. Unlike machine learning community where almost all data and codes are open, in condition monitoring very few things are open, though some people are gradually making codes open. This project is a step towards that direction, even though a tiny one.

This is an ongoing project and modifications and additions of new techniques will be done over time. Python, R, and MATLAB are popular programming languages that are used for machine learning applications. We will use those for our demonstrations. **This page contains results on fault diagnosis only. Results on fault prognosis will be summarized in a separate webpage.**

## Results using [Case Western Reserve University Bearing Data](https://csegroups.case.edu/bearingdatacenter/pages/welcome-case-western-reserve-university-bearing-data-center-website)

1. [SVM on time domain
    features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_multiclass_time.pdf)(Overall accuracy: **96.4%**)
    
2. [SVM on wavelet packet energy features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_energy_multiclass_cwru.pdf) (Overall accuracy: **99.3%**)

3. [Visualizing High Dimensional Data Using Dimensionality Reduction Techniques](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Dimensionality_Reduction.ipynb) ([Python Code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Dimensionality_Reduction.ipynb)) ([R Code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/dimensionality_reduction_projection.pdf))

4. [SVM on wavelet packet entropy features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_entropy_multiclass_cwru.pdf) (Overall accuracy: **99.2%**)

5. [SVM on time and wavelet packet features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/svm_12k_cwru.pdf) (**Achieves 100% test accuracy in one case**)
  
6. [Multiclass Logistic Regression on wavelet packet energy features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression.pdf)(Overall accuracy: **93.8%**)
  
7. [Multiclass Logistic Regression on wavelet packet energy features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression_12k.pdf) (Overall accuracy: **98.8%**)
  
8. [LDA on wavelet packet energy features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_48k.pdf) (Overall accuracy: **88.3%**)
  
9. [LDA on wavelet packet energy features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_12k.pdf) (Overall accuracy: **99.5%**)
  
10. [QDA on wavelet packet energy features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_48k.pdf) (Overall accuracy: **97.7%**)
  
11. [QDA on wavelet packet energy features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_12k.pdf) (Overall accuracy: **99.5%**)
  
12. [kNN on wavelet packet energy features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_48k.pdf) (Overall accuracy: **89%**)
  
13. [kNN on wavelet packet energy features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_12k.pdf) (Overall accuracy: **98.8%**)
  
14. [Decision tree on wavelet packet features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_48k.pdf) (Overall accuracy: **91.3%**)
  
15. [Decision tree on wavelet packet features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_12k.pdf) (Overall accuracy: **98.3%**)
  
16. [Bagging on wavelet packet features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_48k.pdf) (Overall accuracy: **96.8%**)
  
17. [Bagging on wavelet packet features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_12k.pdf) (Overall accuracy: **100%**)
  
18. [Boosting on wavelet packet features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_48k.pdf) (Overall accuracy: **98.6%**)
  
19. [Boosting on wavelet packet features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_12k.pdf) (Overall accuracy: **99.5%**)
  
20. [Random forest on wavelet packet features (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_48k.pdf) (Overall accuracy: **98%**)
  
21. [Random forest on wavelet packet features (12 classes, sampling frequency: 12k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_12k.pdf) (Overall accuracy: **100%**)
  
## Enter Deep Learning

1. [Fault diagnosis using convolutional neural network (CNN) (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Deep_Learning_CWRU_Blog.ipynb) (Overall accuracy: **96.2%**)
  
2. [CNN based fault diagnosis using continuous wavelet transform (CWT) (10 classes, sampling frequency: 48k)](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/CWRU_CNN_Wavelet_Git_Final.ipynb) (Overall accuracy: **98.3%**)
  

(This list will be updated gradually.)

## Some other related stuff

1. [Fault diagnosis of machines (A non-technical introduction)](https://www.awsar-dst.in/assets/winner_article_2018/30_PhD.pdf)

2. [A quick introduction to MATLAB](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/matlab_intro.pdf)

3. [Transient vibration and shock response spectrum plots in MATLAB](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/transient_vibration_and_SRS_plots.pdf)

4. [Simple examples on finding instantaneous frequency using Hilbert transform](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/hilbert_inst_freq_modulation.pdf) ([MATLAB Code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/hilbert_inst_freq_modulation.pdf))

------------------------------
Readers who use the processed datasets of this page **must** cite the original data source as

```
BibTeX citation
@misc{casewesternbearingdata,
  url = {https://csegroups.case.edu/bearingdatacenter/home},
  note = {This data come from Case Western Reserve University Bearing Data Center Website}
}
```
For attribution, readers **may** cite this project as
```
BibTeX citation
@misc{sahoo2016datadriven,
  author = {Sahoo, Biswajit},
  title = Data-Driven Machinery Fault Diagnosis},
  url = {https://biswajitsahoo1111.github.io/cbm_codes_open/},
  year = {2016}
}
```
