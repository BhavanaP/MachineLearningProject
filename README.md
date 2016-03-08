# MachineLearningProject
Classification and Missing value estimation using KNN impute and SVD algorithms,implemented in Matlab & R studio.

Classification

1. Copy all the Training Data, Training labels, Test Data and all the functions in Classification folder into the Matlab Folder – C:\Users\\Documents\MATLAB.
2. Open the Matlab software and declare the variables say Traindata1, Trainlabel1,Testdata1 to save the TrainingData1.txt, TrainLabel1.txt ,TestData1.txt content respectively in the command line.
3. Call the function Keerthana_BhavanaKNN(Traindata1, Trainlabel1) in the command line. This function gives different accuracy values for k=1,2,3,4,5. Consider the k value that has highest accuracy. If needed we can call this function many times to select the k value that gives highest accuracy basing on many observations. Each time we call this function, this gives different accuracies for k=1,2,3,4,5 because we have taken the random split of 80-20 of Training data for training and validation.
4. Now call the function Keerthana_BhavanaResult(Traindata1,Trainlabel1,Testdata1,k). Traindata1,trainlabel1,Testdata1 are variables in which we saved the TrainingData1.txt, TrainLabel1.txt ,TestData1.txt content respectively, and k is the ‘k’ value considered from the above function.
5. Now we can see the labels for the given Testdata1 in the command line.
6. These values are copied into Keerthana_BhavanaClassification1_k=3.txt to have clear reference.

Missing Value Estimation

KNNimpute in Matlab for dataset2:
1. Please copy the given data set files in the matlab folder in C:\Users\\Documents\MATLAB.
2. Now open the matlab software and declare the variables say Dataset2 to save the content in MissingData2.txt.
3. Call the function for Missing values from the command line.
Keerthana_BhavanaMissingValues(Dataset2, k, Output_filename)
Dataset2 is the variable that has MissingData2.txt content, k is the selected k value on many observations and Output_filename is the filename in which we want to save the output file content.
Now we can see the output with all the missing values replaced with predicted values in the output file which will be saved in the same folder.

SVDimpute in R for dataset1 and dataset2:

1. Open R. Set the work directory-
setwd(“path of work directory”)
2. Load the csv file that has the content of MissingData1.txt or FluDataMissingValue.txt in MissingValue Estimation folder-
data=read.csv(“Missingdata3.csv”)
3. R takes the datafile having samples in rows. So if the datafile has samples in rows it is fine else take transpose of that data.
4. Write the command to perform SVDimpute – data1svd=impute.svd(data,9);
5. write.table(data1svd,”C:/Users/Documents/Output.txt”,sep=’\t’)
This is the command to save output in Output.txt file in Documents folder.
