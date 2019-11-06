
# **DAT264x: Identifying Malaria In Blood Imagery** #

----------
## Author ##
*Yuan Jui Huang (黃元瑞)* 

## **Data Description (the details can refer to [MPP](https://www.datasciencecapstone.org/competitions/13/identifying-malaria-in-blood/ "Data Description"))** ##

To predict the infected label, determining whether or not a blood smear sample is infected with malaria. The samples have been giemsa stained, which turns human and parasitic cells purple and pink respectively. You will develop an algorithm that can identify infected samples.

## Preprocessing  ##

1. load image and use data augmentation way to add image variability
	1. Train dataset
	![Alt text](img/train_dataset.png "Train Dataset")
	2. Train dataset with data augmentation
	![Alt text](img/train_dataset_augment.png "Train Dataset")
	3. Valid dataset	
	![Alt text](img/valid_dataset.png "Valid Dataset")
  	4. Test dataset with data augmentation 
	![Alt text](img/valid_dataset_augment.png "Valid Dataset")

2. Create CNN model
![Alt text](img/identifying_malaria.png "Train Dataset")	

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
		2. the confusion matrix 
		![Alt text](img/cm_for_test.png "Train Dataset")	 
		3. the roc curve
		
		![Alt text](img/roc_for_test.png "Train Dataset")	 
4. submisson result
 	![Alt text](img/submissions_result.png "Train Dataset")
