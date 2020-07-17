# MURA_XR_SHOULDER
Binary Classification for normal/abnormal X-ray images on XR_SHOULDER of MURA Data set

# What is MURA?

MURA (musculoskeletal radiographs) is a large dataset of bone X-rays. It is one of the largest public radiographic image datasets. Algorithms are tasked with determining whether an X-ray study is normal or abnormal. 
MURA uses a hidden test set for official evaluation of models. The test set is not publicly readable. 
It consists of 14,863 studies from 12,173 patients, with a total of 40,561 multi-view radiographic images. Each belongs to one of seven standard upper extremity radiographic study types: elbow, finger, forearm, hand, humerus, shoulder, and wrist. Each study was manually labeled as normal or abnormal by board-certified radiologists from the Stanford Hospital.
The MURA dataset can be downloaded from this link : MURA(https://stanfordmlgroup.github.io/competitions/mura/)

# Contents

This repository uses the Shoulder Xray part of the MURA dataset. A densenet model with 169 layers has been used with weights pre-trained on the imagenet dataset. The flatten layer and the binary classification layer are then added and the model is trained on the dataset.
Since the training of these weights takes 5 to 6 hours, the weights of our trained model have been included in the repository by the name “model.h5”. Comments have been added for proper understanding of the code.

# Sample directory structure of dataset – 


-	MURA-v1.1

--	train / valid
	
---	XR_(body part name)

---- patient_id

-----	study(number)_positive/negative

------images(.png)


