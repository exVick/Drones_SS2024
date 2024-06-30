# Drone signature classification
Our solution to case 3 during the “Summer School on Modeling, AI, and Complex Systems ‘2024”: https://github.com/Marchev-Science/case-drone-signature-classification

## 1. The tasks we had
Use the provided CardRF dataset to solve the following tasks:
1. Extract characteristic features for every UAV, distinguishing it from the others.
2. Use the features to classify (through a multi-class model) to determine the type of UAV.
3. Use the features to determine which activities the UAV is doing.
4. Distinguish LOS/NLOS.

## 2. The CardRF Dataset

### INTRODUCTION

TABLE I: Catalog of RF devices used in the experiment for 2.4 GHz RF fingerprint acquisition

![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/c99312ce-1b28-499a-8276-1bdf54894304)

### DATA ACQUISITION
![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/900d9a9a-bbd7-4d64-9537-bd8253a6b675)
Fig. : The RFSSCS setup for visual line of sight capturing of signals from : (a) a UAV controller, (b) a UAV (DJI Matrice 600).


![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/da93b97a-38b6-4815-8ab3-deec302b9695)
Fig. : The RFSSCS setup for beyond-visual-line-of-sight capturing of signals from UAV.

### DATA STRUCTURE
Illustration tree of the directories
![image](https://github.com/exVick/case-drone-signature-classification/assets/91212676/efc36ec4-4c76-4252-a016-6899318717d0)
Fig. : Directory tree for data label of the Cardinal RF dataset, showing the UAV models and UAV flight modes as sub-directories and sub-directories of sub-directories, respectively.





## References 

[1] GitHub Case Drone signature classification. [Online]. Available: https://github.com/Marchev-Science/case-drone-signature-classification/tree/main.

[2] O. O. Medaiyese, M. Ezuma, A. P. Lauf, and A. A. Adeniran, “Hierarchical Learning Framework for UAV Detection and Identification” arXiv preprint arXiv: 2107.04908, 2021.

[3] AERPAW, “CARDINAL RF (CARDRF): An Outdoor UAV/UAS/DRONE RF Signals with Bluetooth and WiFi Signals Dataset”. [Online]. Available: https://aerpaw.org/dataset/cardinal-rf-cardrf-an-outdoor-uav-uas-drone-rf-signals-with-bluetooth-and-wifi-signals-dataset/

[4] scikit-learn, Decision Trees. [Online]. Available: https://scikit-learn.org/stable/modules/tree.html

