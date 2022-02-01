# Deep learning connects DNA traces totranscription to reveal predictive features beyondenhancer–promoter contact
## Abstract
Problem and Objectives:
1. Super-resolution microscopy made measuring chromatin 3D structure possible but hard to employ it using computational methods.
2. Using deep learning methods to explore the relationship between chromatin structure and transcription state of single cells.
3. Exploring methods to “unpack the blackbox” to determine which structural features of chromatin regulationare most important for gene expression state. 

Dataset and Result:
1. An Optical Reconstruction of Chromatin Architecture dataset of the Bithorax gene cluster in Drosophila 
2. It outperforms previous contact-focused methods in predicting expression state from 3D structure. 

Conclusions:
1. We find the structural information is distributed across the domain, overlapping and extending beyond domains identified by prior genetic analyses. 
2. Individual enhancer-promoter interactions are a minor contributor to predictions of activity.

## Introduction
1. Bulk approaches measure limited aspects of structure, such as contact interactions, and observe only population level averaged structural features and averaged expression states rather than the features of individual cells.
2. In contrast, imaging approaches can directly measure the dis- tances between elements, such as the position of a distal enhancer and its target promoter, in single cells.
3. Therefore, in order to 
  (1) address more thoroughly to what degree chromatin structure relates to the transcriptional state of individual cells and 
  (2) determine in an unbiased manner, which structural features of chromatin regulation are most important
  we developed a deep learning-based approach, which is threshold free, and can account for a wide variety of complex structure-expression relationships.
4. Dataset: tis data set contained over 50,000 cells, in each of which the 3D structure of BX-C gene cluster was imaged with ORCA and nascent RNA expression for each of the three hox genes measured with fluorescent in situ hybridization targeting ribonucleic acid molecules (RNA FISH).

## Methods
1. First remove features that reflected technical rather than biological differences in the chromatin structure data. For example, the (x,y,z) coordinates measured for the polymer are recorded relative to the microscope stage axis. Viewing the same structure from two different angles results in different (x,y,z) values, which do not reflect a biological difference in structure. We addressed this challenge by calculating the relative distances between all 52 positions along with the polymer, represented as a 52 × 52 matrix, thereby preserving all structural features except the experimental viewing angle. Missing data values were estimated by linear interpolation between the adjacent (x,y,z) coordinates. All distances were then normalized relative to the average inter- position distances to accentuate differences. To facilitate deep learning, we classified nascent RNA expression into ON or OFF binary classes.
![image](https://github.com/XueminZhu-Charmaine/Papers/blob/main/images/DeepDNA_fig1.png)
2. 2D CNNs start with an input data matrix (image), which is passed through a series of filters (convolutions). The transformed data are then passed through a data integration layer or a pooling layer. CNNs are often built with pairs of convolutional (filter) layers and pooling layers. The output of one or more rounds of convolu- tional followed by pooling layers is then flattened by being fed into a series of dense neural network layers, which output a final prediction. The network is optimized to maximum performance through iterative training rounds, where predictions are compared with the ground truth training labels, generating a loss measurement between the performance of the CNN and the maximal possible performance. Using this loss measurement, weights of the network are optimized through a method known as back propagation. This iterative process is repeated until the loss stabilizes.
