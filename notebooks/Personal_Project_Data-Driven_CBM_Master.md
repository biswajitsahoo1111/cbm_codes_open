## Introduction to the problem

Condition based maintenance is the process of doing maintenance only
when it is required. This has many advantages along with monetary gain
as it precludes periodic maintenance and reduces unplanned downtime. The
next logical question is to figure out when maintenance is required.
Maintenance is required if fault has either occurred or is imminent.
This leads us to the problem of fault diagnosis and prognostics.

In fault diagnosis, fault has already occurred and our aim is to find
what type of fault is there and what is its severity. In fault
prognostics out aim is to predict the time of occurrence of fault in
future, given its present state. These two problem are central to
condition based maintenance. There are many methods to solve these
problems. These methods can be broadly divided into two groups:

  - Model Based Approach
  - Data-Driven Approach

In model based a complete model of the system is formulated and it is
then used for fault diagnosis and prognostics. But this method has
several limitations. Firstly, it is a difficult task to accurately model
a system. Modelling becomes even more challenging with variations in
working conditions. Secondly, we have to formulate different models for
different tasks. For example, to diagnose bearing fault and gear fault,
we have to formulate two different models. Data-driven methods provide a
convenient alternative to these problems.

In data-driven approach, we use operational data of the machine to
design algorithms that are then used for fault diagnosis and
prognostics. The operational data may be vibration data, thermal imaging
data, acoustic emission data, or something else. These techniques are
robust to environmental variations. Accuracy obtained by data-driven
methods is also at par and sometimes even better than accuracy obtained
by model based approaches. Due to these reasons data-driven methods are
becoming increasingly popular at diagnosis and prognostics tasks.

## Aim of the project

In this project we will apply some of the standard techniques to
publicly available data sets and show their results with code. There are
not many publicly available data sets in machinery condition monitoring.
But we will only use those data sets that are publicly available. Unlike
machine learning community where almost all data and codes are open, in
condition monitoring very few things are open, though some people are
gradually making codes open. This project is a step towards that
direction, even though a tiny one.

This is an ongoing project and modifications and additions of new
techniques will be done over time. Python, R, and MATLAB are three
popular programming languages that can be used for machine learning
applications. We will use one of those for our demonstrations.

## Results

1.  [Multiclass bearing fault classifical using SVM on time domain
    features](https://github.com/biswajitsahoo1111/cbm_codes_open/blob/master/notebooks/SVM_multiclass_time.pdf)
    (On [Case Western Reserve University Bearing
    Data](https://csegroups.case.edu/bearingdatacenter/pages/welcome-case-western-reserve-university-bearing-data-center-website))
