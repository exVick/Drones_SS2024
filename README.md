# Drone signature classification
Our solution to case 3 during the “Summer School on Modeling, AI, and Complex Systems ‘2024”: https://github.com/Marchev-Science/case-drone-signature-classification

## 1. The tasks we had
Use the provided CardRF dataset to solve the following tasks:
1. Extract characteristic features for every UAV, distinguishing it from the others.
2. Use the features to classify (through a multi-class model) to determine the type of UAV.
3. Use the features to determine which activities the UAV is doing.
4. Distinguish LOS/NLOS.

## 2. The CardRF Dataset

Original authors:  
Olusiji O Medaiyese (email:medaiyese09@gmail.com)  
Martins Ezuma (email: mcezuma@ncsu.edu)  
Adrian P Lauf (email:adrian.lauf@louisville.edu)  
Ayodeji A Adeniran (email:aaaden02@louisville.edu)

Editor:
Angel Marchev, Jr.

### INTRODUCTION

In this work, we curated an open-source dataset called the Cardinal RF dataset, abbreviated as the CardRF dataset. Here, both the UAV and UAV flight controller signals from six UAS (unmanned aerial systems), WiFi signals from two WiFi devices, and Bluetooth signals from five devices are used to acquire the CardRF dataset in an outdoor environment. The device catalogue (UAS, Bluetooth, and WiFi) is listed in Table I. The Bluetooth and WiFi devices are used to acquire Bluetooth and WiFi signals, respectively. Similarly, two components (i.e., UAV and its flight controller) of a UAS are utilized in collecting the UAS signals.

TABLE I
Catalog of RF devices used in the experiment for 2.4 GHz RF fingerprint acquisition (in red are the devices we had).
![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/c99312ce-1b28-499a-8276-1bdf54894304)

### EXPERIMENTAL MODEL AND DESIGN

The experimental model and design have been discussed in [2].

### DATA ACQUISITION

The data acquisition is categorized into visual line-of-sight (VLOS) and beyond-visual-line-of-sight (BVLOS) data collection.
1) Visual Line of Sight (VLOS): In VLOS data collection, there is no obstruction between the RF signal sensing and capturing system (RFSSCS) and the device (e.g., UAV, UAV controller). Signals are captured at a distance range of 8-12 meters.

2) Non-Visual-Line-of-Sight (NVLOS): In NVLOS data collection, an obstruction exists between the RFSSCS and the devices to analyze multi-path fading or other channel effects. Signals from three UAVs (DJI Inspire, DJI Matrice 600, DJI Phantom) are captured.

![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/900d9a9a-bbd7-4d64-9537-bd8253a6b675)
Fig. 1: The RFSSCS setup for visual line of sight capturing of signals from: (a) a UAV controller, (b) a UAV (DJI Matrice 600).


![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/da93b97a-38b6-4815-8ab3-deec302b9695)

Fig. 2: The RFSSCS setup for beyond-visual-line-of-sight capturing of signals from UAV.

### DATA AND FILE STRUCTURE

The CARDRF directory contains the raw signals, from which the LOS examples are already divided into train and test sets. The Processed CardRF directory includes the sliced steady signals from LOS, each labeled with the respective class. Each signal in this directory has 1024 sampling points. The MATLAB code used for processing these signals is located in the code directory. The raw signals needed to be scaled using a factor of 6.581e−06 for the voltage.

![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/efc36ec4-4c76-4252-a016-6899318717d0)
Fig. 3: Directory tree for data label of the Cardinal RF dataset, showing the UAV models and UAV flight modes as sub-directories and sub-directories of sub-directories, respectively.

* File naming convention:
```
BEEBEERUN_0000100001.mat_data.csv  
,where  
BEEBEERUN_00001 - device name and model  
00001 - consecutive number of experiment (some of them are missing)  
.mat - file extention (we should have removed it, but we did not)
_data.csv / _meta.csv - data type recorded in the file - 'data' for raw data, 'meta' - for metadata
```

## 3. Our Solutions

### 1. Extract characteristic features for every UAV, distinguishing it from the others.

### 2. Use the features to classify (through a multi-class model) to determine the type of UAV.

### 3. Use the features to determine which activities the UAV is doing.

### 4. Distinguish LOS/NLOS.
Beyond scope of our work.


## References 

[1] GitHub Case Drone signature classification. [Online]. Available: https://github.com/Marchev-Science/case-drone-signature-classification/tree/main.

[2] O. O. Medaiyese, M. Ezuma, A. P. Lauf, and A. A. Adeniran, “Hierarchical Learning Framework for UAV Detection and Identification” arXiv preprint arXiv: 2107.04908, 2021.

[3] AERPAW, “CARDINAL RF (CARDRF): An Outdoor UAV/UAS/DRONE RF Signals with Bluetooth and WiFi Signals Dataset”. [Online]. Available: https://aerpaw.org/dataset/cardinal-rf-cardrf-an-outdoor-uav-uas-drone-rf-signals-with-bluetooth-and-wifi-signals-dataset/

[4] scikit-learn, Decision Trees. [Online]. Available: https://scikit-learn.org/stable/modules/tree.html

