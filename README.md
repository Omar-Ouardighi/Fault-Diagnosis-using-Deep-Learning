# Convolutional neural networks (CNN) for bearings faults classification

In this repository, we will show results of fault diagnosis task using deep learning on the  Case Western Reserve University bearing dataset.

# Data

We have used CWRU data for this demonstration. It is a standard database used in condition monitoring applications. We have used the drive end data that are sampled at 48 kHz sampling frequency when load of 1 hp is applied on the shaft. Normal data collected with 1 hp load have also been used. There are a total of 10 classes. The classes are

   - C1 : Ball defect (0.007 inch, load: 1 hp)
   - C2 : Ball defect (0.014 inch, load: 1 hp)
   - C3 : Ball defect (0.021 inch, load: 1 hp)
   - C4 : Inner race fault (0.007 inch, load: 1 hp)
   - C5 : Inner race fault (0.014 inch, load: 1 hp)
   - C6 : Inner race fault (0.021 inch, load: 1 hp)
   - C7 : Normal (load: 1 hp)
   - C8 : Outer race fault (0.007 inch, load: 1 hp, data collected from 6 O'clock position)
   - C9 : Outer race fault (0.014 inch, load: 1 hp, 6 O'clock)
   - C10 : Outer race fault (0.021 inch, load: 1 hp, 6 O'clock)

From each category data are collected in segments of length 1024 and resized to a 2-D matrix of size (32 by 32). There is no overlap between segments. For each category 460 such segments are taken. Total size of the data thus becomes (4600, 32, 32). Out of this 1000 segments are randomly chosen as test data and rest are used for training.


## SOURCES
- https://ieeexplore.ieee.org/document/8114247
- https://engineering.case.edu/bearingdatacenter
- https://biswajitsahoo1111.github.io/cbm_codes_open/
