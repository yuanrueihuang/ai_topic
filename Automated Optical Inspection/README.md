
# **【廣達電腦徵才】自動光學檢測領域** #

----------
## Author ##
*Yuan Jui Huang (黃元瑞)* 

## **Data Description (the details can refer to [Aldea](https://aidea-web.tw/topic/5670ac89-f834-4f08-a9e0-22d968c15e64 "Data Description"))** ##

Automated optical inspection (AOI) [1] is an automated visual inspection of printed circuit board (PCB) (or LCD,transistor) manufacture where a camera autonomously scans the device under test for both catastrophic failure (e.g. missing component) and quality defects (e.g. fillet size or shape or component skew).

Reference
[1] https://en.wikipedia.org/wiki/Automated_optical_inspection

## Preprocessing  ##

1. load image and use data augmentation way to add image variability
	1. Train dataset
	![Alt text](img/train0_dataset.png "Train Dataset")
	![Alt text](img/train1_dataset.png "Train Dataset")
	![Alt text](img/train2_dataset.png "Train Dataset")
	![Alt text](img/train3_dataset.png "Train Dataset")
	![Alt text](img/train4_dataset.png "Train Dataset")
	![Alt text](img/train5_dataset.png "Train Dataset")
	2. Train dataset with data augmentation (with scale, blur)
	![Alt text](img/train_dataset_augment.png "Train Dataset")
	3. Valid dataset	
	![Alt text](img/valid0_dataset.png "Valid Dataset")
	![Alt text](img/valid1_dataset.png "Valid Dataset")
	![Alt text](img/valid2_dataset.png "Valid Dataset")
	![Alt text](img/valid3_dataset.png "Valid Dataset")
	![Alt text](img/valid4_dataset.png "Valid Dataset")
	![Alt text](img/valid5_dataset.png "Valid Dataset")
  	4. Valid dataset with data augmentation (with scale, blur)
	![Alt text](img/valid_dataset_augment.png "Valid Dataset")

2. Create CNN model
![Alt text](img/aoi.png "Train Dataset")	

3. Evaluation model
	1. train dataset and valid dataset (without data augmentation)
		1. the loss and accuracy of train dataset and valid dataset
		![Alt text](img/loss_for_train_valid.png "Train Dataset")	 
		2. the confusion matrix of train dataset and valid dataset
		![Alt text](img/cm_for_train_valid.png "Train Dataset")
		3. the roc curve of train dataset and valid data		
		![Alt text](img/roc_for_train_valid.png "Train Dataset")

	2. test dataset (use valid dataset with data augmentation)
		1. the loss and accuracy 
		![Alt text](img/loss_for_test.png "Train Dataset") 
		2. the average loss and the roc curve, the confusion matrix 
		![Alt text](img/avgloss_cm_roc_for_test.png "Train Dataset")			 

4. submisson result
 	![Alt text](img/submissions_result.png "Train Dataset")
