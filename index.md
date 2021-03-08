# Malware Detection 
Authors: [**Yikai Hao**](https://github.com/YikaiHao), [**Yu-Chieh Chen**](https://github.com/yuc399), [**Ruoyu Liu**](https://github.com/rul141)

[Check on GitHub Repo](https://github.com/YikaiHao/DSC180_Winter)

## Overview
As the technology grows fast in recent years, more and more people cannot live without cell phones. It is important to protect users’ data for cell phone companies and operating system providers. Therefore, detecting malwares based on the code they have can avoid publishing of malwares and prohibiting them from the source. This report aims at finding a model which can detect malwares accurately and with a small computational cost. It uses different matrices and graphs to search the relationships between applications and detecting malwares based on the similarity. As a result, the best model can achieve a test accuracy around 99%.

## Data Generating Process
### Data Description
The data source is called Android Malware Dataset (AMD). The dataset is published in 2017 by the Argus Lab from the University of South Florida. This data source is used by many other malware detection papers and widely used in the research domain. We then extract the smali file after decompiling the APK(Android Application Package).

### Smali 
In order to analyze the smali files, we should understand the structure of it. Therefore, here is the description of the smali files and the features contained in the smali files.

### API Calls
In order to understand which part of the smali files do the malicious action, we put our attention on API (Application Programming Interface) calls. There are four main components in an API call.

### Database 
We design a new database for storing data.

## Model 
### Feature Distribution
In order to check whether the features we generate are useful for checking malwares, some Exploratory Data Analysis (EDA) has done on features. We check the difference between unique values among features considered the type of applications. The result shows that our features can clearly identify the different types of applications since the value between different types of applications are large. 

As we can see from the graphs, the distribution of every application type for every feature is different.

### Hindroid 
HinDroid is the baseline model we use for our report. It contains different types of kernels and the meaning behind each kernel is different. It uses the features we extract from the data generating process to build some matrices. Each matrix shows a type of relationship between apis or applications. Each matrix is an adjacent matrix for a graph with a specialized relationship. By choosing different types of matrices we want to combine together, we get the kernel we have. Then we will be able to use the custom kernels and put in different classifiers like SVM or Random Forest for malware detection. 

### Word2Vec
The HinDroid model runs pretty slow since there are a large number of APIs. However, lots of APIs only appear once among all applications and they are meaningless for detecting malwares. In addition, there are also some APIs which appeared in almost every application. Those APIs are also not meaningful enough to help us pick out the malwares. Therefore, new models are being considered and built. Based on the logic of HinDroid, we try to develop some new matrices to replace the original matrices which will have a faster speed and similar accuracy.


### Node2Vec

### Metapath2Vec

### New Model 

## Result 

### Classifiers 

### Result Tables 
#### HinDroid

#### Word2Vec

#### Node2Vec

#### Metapath2Vec

#### New Model 

## Conclusion 

## Future Work 

## Reference 
