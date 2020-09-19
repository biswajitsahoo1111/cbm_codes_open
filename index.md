Condition based maintenance (CBM) is the process of doing maintenance only when it is required. Adoption of this maintenance strategy leads to significant monetary gains as it precludes periodic maintenance and reduces unplanned downtime. Another term commonly used for condition based maintenance is predictive maintenance. As the name suggests, in this method we predict in advance when to perform maintenance. Maintenance is required, if fault has already occurred or is imminent. This leads us to the problem of fault diagnosis and prognosis.

In fault diagnosis, fault has already occurred and our aim is to find what type of fault is there and what is its severity. In fault prognosis, our aim is to predict the time of occurrence of fault in future, given its present state. These two problem are central to condition based maintenance. There are many methods to solve these problems. These methods can be broadly divided into two groups:

  - Model Based Approaches
  - Data-Driven Approaches

In model based approach, a complete model of the system is formulated and it is then used for fault diagnosis and prognosis. But this method has several limitations. Firstly, it is a difficult task to accurately model a system. Modelling becomes even more challenging with variations in working conditions. Secondly, we have to formulate different models for different tasks. For example, to diagnose bearing fault and gear fault, we have to formulate two different models. Data-driven methods provide a convenient alternative to these problems.

In data-driven approach, we use operational data of the machine to design algorithms that are then used for fault diagnosis and prognosis. The operational data may be vibration data, thermal imaging data, acoustic emission data, or something else. These techniques are robust to environmental variations. Accuracy obtained by data-driven methods is also at par and sometimes even better than accuracy obtained by model based approaches. Due to these reasons data-driven methods are becoming increasingly popular at diagnosis and prognosis tasks.

## Aim of the project

In this project we will apply some of the standard machine learning techniques to publicly available data sets and show their results with code. There are not many publicly available data sets in machinery condition monitoring. So we will manage with those that are publicly available. Unlike machine learning community where almost all data and codes are open, in condition monitoring very few things are open, though some people are gradually making codes open. This project is a step towards that direction, even though a tiny one.

This is an ongoing project and modifications and additions of new techniques will be done over time. **Python** and **R** are popular programming languages that are used for machine learning applications. We will use those for our demonstrations. **Tensorflow** will be used for deep learning applications. This page contains results on fault diagnosis only. Results on fault prognosis can be found [here](https://biswajitsahoo1111.github.io/rul_codes_open).

## Results using [Case Western Reserve University Bearing Data](https://csegroups.case.edu/bearingdatacenter/pages/welcome-case-western-reserve-university-bearing-data-center-website)<sup>*</sup>
-------------------------------
We will first apply classical feature based methods (so-called shallow learning methods) to obtain results and then apply deep learning based methods. In feature based methods, we will extensively use [wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/calculate_wavelet_packet_energy_features.ipynb) and [wavelet packet entropy featues](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/calculate_wavelet_packet_entropy_features.ipynb) that are calculated from raw time domain data. Dataset description and [time domain preprocessing](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/CWRU_time_domain_data_preprocessing.ipynb) steps can be found [here](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/CWRU_time_domain_data_preprocessing.ipynb). The procedure detailing calculation of wavelet packet energy features can be found at [this link](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/calculate_wavelet_packet_energy_features.ipynb) and similar calculations for wavelet packet entropy features can be found at [this link](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/calculate_wavelet_packet_entropy_features.ipynb).

1. [SVM on time domain
    features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_multiclass_time_cwru_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **96.5%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_multiclass_time_cwru_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_multiclass_time.pdf))
    
2. [SVM on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_energy_multiclass_cwru_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **99.3%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_energy_multiclass_cwru_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_energy_multiclass_cwru.pdf)) 

3. [Visualizing High Dimensional Data Using Dimensionality Reduction Techniques](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Dimensionality_Reduction.ipynb) ([Python Code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Dimensionality_Reduction.ipynb)) ([R Code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/dimensionality_reduction_projection.pdf))

4. [SVM on wavelet packet entropy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_entropy_multiclass_cwru_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **99.3%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_entropy_multiclass_cwru_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_wavelet_entropy_multiclass_cwru.pdf)) 

5. [SVM on time and wavelet packet features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/svm_12k_cwru_python.ipynb) (12 classes, sampling frequency: 12k) (**Achieves 100% test accuracy in one case**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/svm_12k_cwru_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/svm_12k_cwru.pdf)) 
  
6. [Multiclass Logistic Regression on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **98.5%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression.pdf))
  
7. [Multiclass Logistic Regression on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **99.7%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/multiclass_logistic_regression_12k.pdf)) 
  
8. [LDA on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **89.8%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_48k.pdf)) 
  
9. [LDA on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **99.5%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/LDA_12k.pdf)) 
  
10. [QDA on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **96.5%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_48k.pdf)) 
  
11. [QDA on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **99%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/QDA_12k.pdf)) 
  
12. [kNN on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **89.8%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_48k.pdf)) 
  
13. [kNN on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **99.5%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/kNN_12k.pdf)) 
  
14. [Decision tree on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **94.5%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_48k.pdf)) 
  
15. [Decision tree on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **99.7%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/decision_tree_12k.pdf)) 
  
16. [Bagging on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **97%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_48k.pdf)) 
  
17. [Bagging on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **100%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/bagging_12k.pdf)) 
  
18. [Boosting on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **99%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_48k.pdf)) 
  
19. [Boosting on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **100%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/boosting_12k.pdf)) 
  
20. [Random forest on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_48k_python.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **98.1%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_48k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_48k.pdf)) 
  
21. [Random forest on wavelet packet energy features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_12k_python.ipynb) (12 classes, sampling frequency: 12k) (Overall accuracy: **100%**) ([Python code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_12k_python.ipynb)) ([R code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/random_forest_12k.pdf)) 

<sup>*</sup> This hyperlink points to the actual website of CWRU bearing dataset. Unfortunately, it has been recently observed that the original website remains down most of the time. As the dataset is well known, it can still be found on the internet at different places. Interested readers who want to experiment with this dataset can find it [here](https://data.mendeley.com/datasets/fkp3nn4tp7/1#folder-a8bb9715-4b7b-4fa1-8550-5b0cdcf62602) (If it's not down). Actual data are stored in `.mat` format. But the data in previous link are first extracted from `.mat` format and then individually stored in `.csv` format. Readers should first try to download the data from the original website. If that attempt fails, they should explore other options.
  
## Enter Deep Learning

--------------------------

In this section, we will show results of fault diagnosis task using deep learning on the same Case Western Reserve University bearing dataset. Due to the nondeterministic nature of operations used in deep learning and dependence of libraries like `Tensorflow` on computer architecture, readers might obtain slightly different results than those in the notebooks. As a more reliable measure, we report average results of ten iterations. Our models are small enough to permit us to run those that many times in a reasonable amount of time. For reproducibility of our results, we also share the saved models of each notebook. All saved models can be found at [this link](https://github.com/biswajitsahoo1111/cbm_codes_open/tree/master/notebooks/saved_models). A notebook describing the steps to use the saved models can be found [here](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Using_saved_models_tensorflow.ipynb).

1. [Fault diagnosis using convolutional neural network (CNN) on raw time domain data](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Deep_learning_based_fault_diagnosis_using_CNN_on_raw_time_domain_data.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **98.7%**)
  
2. [CNN based fault diagnosis using continuous wavelet transform (CWT) of time domain data](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/Deep_learning_based_fault_diagnosis_using_CNN_on_continuous_wavelet_transform_of_time_data.ipynb) (10 classes, sampling frequency: 48k) (Overall accuracy: **99.1%**)
  

(This list will be updated gradually.)

### Why have I used only Jupyter notebooks?

These notebooks are for educational purposes only. Our experiments are relatively small scale and can be run in a reasonable amount of time in a notebook. I personally love the interactive nature of jupyter notebooks. We can see what we are doing. So the answer to the above question is: personal choice. I also don't intend to deploy these, at least for the time being, in a production environment. Readers who wish to build deployment ready systems should bear in mind that they have to do many other things than just run an algorithm in a jupyter notebook.

## Some other related stuff

-------------------------------

1. [Data-Driven Remaining Useful Life (RUL) Prediction](https://biswajitsahoo1111.github.io/rul_codes_open/) 

2. [Fault diagnosis of machines (A non-technical introduction)](https://biswajitsahoo1111.github.io/post/fault-diagnosis-of-machines/)

3. [Blog articles by yours truly](https://biswajitsahoo1111.github.io/categories/blog/)

4. [A quick introduction to MATLAB](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/matlab_intro.pdf)

5. [Transient vibration and shock response spectrum plots in MATLAB](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/transient_vibration_and_SRS_plots.pdf)

6. [Simple examples on finding instantaneous frequency using Hilbert transform](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/hilbert_inst_freq_modulation.pdf) ([MATLAB Code](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/hilbert_inst_freq_modulation.pdf))

------------------------------

For attribution, cite this project as
```
BibTeX citation
@misc{sahoo2016datadriven,
  author = {Sahoo, Biswajit},
  title = {Data-Driven Machinery Fault Diagnosis},
  url = {https://biswajitsahoo1111.github.io/cbm_codes_open/},
  year = {2016}
}
```
Readers should cite original datasets separately.
