# Identify the snake breed

### Problem statement
The government has been facing a long-standing issue of wild animals entering residential areas due to various reasons. It's of critical importance that if any such dangerous 
animal is encountered, the concerned authority should be notified immediately. Reptiles, especially snakes, are among the most dangerous animals and they often enter residential
areas. Recently due to an incident of a youngster getting bitten by a snake, the government decided to install cameras at every corner of the road to detect snakes and other 
animals.You have been hired as a Deep Learning engineer to create a sophisticated model that can detect the breed of a snake from its image.

### Data description
This data set consists of the following two columns:
* image_id	= Name of the image file
* breed	- Snake breed [35 different breeds]
* The data folder consists of two folders and two .csv files. The details are as follows:
* train: Contains 5508 images for 35 classes 
* test: Contains 2361 images
* train.csv: 5508 x 2
* test.csv: 2361 x 1

### Evaluation metric
score = {100* f1\_score(actual\_values,predicted\_values,average = 'weighted')}
