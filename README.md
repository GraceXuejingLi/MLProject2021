## Spring 2021 
## PROJECTS IN ADVANCED MACHINE LEARNING (GR5054)
This folder contains all the assignments for Advanced Machine Learning, including mini-hackathon projects exploring tabular, image, and text data.

Created and completed by Grace Xuejing Li

### [Project 1: U.N. World Happiness Tabluar Data Exercise] ()

#### Description:
Used U.N. World Happiness Data and built machine learning models to predict each country's happiness level.
Started with exploratory data analysis to explore patterns between certain features and the target vairable.
Understanding Data: Check columns, data type, null values, shape, etc..
Build graphs to explore bivariate relationships between feautres and the target vairables to draw insights for modeling.
Get ride of Outliers

#### Finding: Features such us GDP per capita, Freedom to make life choices, Social support, Healthy life expectancy all have a positive correlation with people's happiness level.
#### Data:
U.N. World Happiness Data

#### Model Performance:
Automatic Feature Selection using Random Forest classifier and retained 6 out of 10 features in total
KNN Classification
Test data performance score: 0.38
Used gridsearchCV to find the best parameter
Random Forrest
Accuracy on test set: 0.269
Keras
Accuracy: 42%

### [Project 2: Covid Positive X-Ray Image Data] ()

#### Description:
 State-of-the-art image processing techniques are being widely used in the diagnosis of diseases by processing medical images such as X-rays, MRIs, and others. Compared to more traditional techniques that are more expensive, less accurate and requires special medical personnel, training computers to diagnose diseases or facilitate surgeries becomes a more popular choice becasue of it's versatility and efficiency.

   These comparative advanges of computer vision techniques become espicially evident at the disastrous shock of the Coronavirus pandemic disease which put the hospital system, human resilience, and our ability to quickly adapt technology to test. Prompt response to the pandemic requires state-of-the-art computer vision technologies and applying it to the early diagnose and treatment of the disease, among others. Therefore, building models that could accurately predict COVID-19 infection and gathering datas to train these models become the primary tasks of researchers.

   The dataset is a collection of chest X-ray images from six different databases. The COVID-19 databse is collected by the author from publicly avaible databases, whie normal and viral pneumonia databases are collected from publicly avaible Kaggle databases. Details of each database is summarized in the original paper.


#### Data:
X-ray image data of Covid-19 patients

#### Model:
Squeezenet Model
Validation accuracy score: 0.64
VGG16 Model
Resnet Model with Transfer Learning

#### Findings:
 Overall, our first model, Squeezenet, has the best performance among the other models. The nypterparameter, epoch, is set to four, which means the model runs through the entire training dataset four times. To avoid overfitting on the trainning dataset, I also added two dropout of 0.5 layers to the model. The dropout layer will randomly switch off 50% of the neurons and reduce model complexity. Our third model has a significantly higher accuracy score than the validation accuracy score, which means the model is overfitting on the training dataset. 

### [Project 3: Covid Tweets Misinformation] ()
#### Description:
The data was collected from two different sources. The first data set consists of false or partially dalse tweetst from fact-checking websites, and the second source comes frmo a random sample of tweets realted to COVID-19. Although the defination of misinformation remains controversial, the researchers defined it as"circulating information that is false", distinguishing from the more commonly used defination for misinformation and disinformation. 

One of the greattest advantages of building a machine learning model for social media text analysis is it's versatility and temporality. Even though informations on Twitter API is still very limited, one could still build upon the API and inform various research areas. From ethical debates, political schemes, and to media criticism, the various topics where text analysis machine learning model could contribute are all still evolving. These types of technique and research practice not only breaks the gap of scientific researches in various areas, but it also helps to make the information circulating online more transparent to the public. Technique practices like building model to classify texts complements areas where theoretical studies might have a lack of. And together, they could help to answer questions such as what kind of information are circulated on social media, how does certain infomation spread virally, and more importantly how does the control of information ciruclated on social media creates or subverts powers. 


#### Data:
Covid Tweets misinformation data

#### Model:
Used Emedding Layers and One LSTM layer
Validation accuracy score: 0.92
Bidirectional LSTM Layer
Validation accuracy score: 0.93
Dropout Regularization LSTM Model
Validation accuracy score: 0.94
Embedding Layers and One 1D Convolution Layer Model
Validation accuracy score: 0.44

 In general, the three models with LTSM layer performed similarily well. The second model with bidirectional LSTM with dropout regularization performed the best with a validation accuracy score of 93.6. In the text analysis, the sequential order of words and phrases is not critical for us to interprete the semantic meaning. Therefore applying bidirectional, the model will process the sequence from both ways, which means the bidirectional model might be able o catch patterns overlooked by a regular technique. With some dropout regularizations, models with the bidirectional technique could potentially significantly improve performances. 
