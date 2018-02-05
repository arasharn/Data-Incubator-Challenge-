# Data Breach Prevention in Big Companies
## Data Incubator Challenge Project Proposal - Arash Nouri
### Abstract:
***Every high-tech company afraid of transferring their technology to their rivals by their left employees.One of the way to prevent this problem is to predict the leaving employees and limited their access to the sensitive information. This project is trying to detect any suspicious behavior of eployees of a company, by analyzing thier acticvities such as eamial, browser history, sign up hour, esployment statue, file transfered, "O, C, E, A, N" score. The main goal of this study is to detect any pattern amoung the employees, who live the company and detect any suspicus activities before that. In the next step a network anaysis will be done to analyze the network of the pepople who left the company to find out if there was any recruter amoung the employees.***   
### Motivation
Data breach is a worse nightmare of a high-tech company. As a result they try to track the on-premise activities of employees as much as possible, generating massive amounts of **data**. A comprehensive data minig is done on the data of two companies. the final product of this study will a several claasifier and regressor, which can be used by HR of companies for recogonizing the leaving employees and prediciting the length of work of each eaployee by analyzing the peronality and their online activities. 
### Data
Data of two companies is used in this project that in total it would a 18 GB of data. Each data set, contains the log on/off activities, websites addresses, date of the activity, device ID, O, C, E, A, N score, employment statue, employment ID, type of the transfered and attached files. *Small portion of data was used for this proposal as a pre-analysis report.*   
A small portion of data set can be found [here](http://www.apps.stat.vt.edu/leman/VTCourses/DataSets1_9182017.zip) and     
#### Feature engineering
The initial features are unsufficient, thus feature engineering needs to be done on the features and new features needs to be created out of the original features. There are different type of the features on the data set:   
1. Date/Time based features   
2. Activity features (sign on/off)   
3. Identification data   
4. Transfered files   
5. Sentiments

At the begining tried to maled the differetn time features by using the date data, for beeter patter visualizition. By using the websites address, their domain were extracted. Then a pre-trained lexicon was used to find the polarity of websites names. *More data analytics needs to be done on the email addresses, reciever of the emails, type of the transferred files, and sentiment analysis websited and emails*   
#### Initial results
The codes for initial data analysis are [here](https://github.com/arasharn/Data-Incubator-Challenge-/blob/master/lt1.ipynb) and [here](https://github.com/arasharn/Data-Incubator-Challenge-/blob/master/lt2.ipynb). Features in the are as follows:   

Feature name | Feature Description            | Source in the Original Dataset 
-------------|--------------------------------|-------------------------------
year         | Year                           | date
month        | Month number                   | date
week         | Week number in a year          | date
time         | Time of the day                | date
numdate      | Date                           | date
PC           | PC ID                          | pc
user_cat     | User ID                        | user
polarity     | Polarity of websites names     | website
subjectivity | Subjectivity of websites names | website                
domain_cat   | Domains of websites            | website   
     
![corr]
(https://github.com/arasharn/Data-Incubator-Challenge-/blob/master/corr.png?raw=true)   
[Figure 1](#corr) shows, the correlation between each of features.   
    
![visit]
(https://github.com/arasharn/Data-Incubator-Challenge-/blob/master/visitis.png?raw=true)   
[Figure 2](#visit) illustrates that all web sites are not important. For example *.com* domain is very generic but domians like *.org* or *.gov* are more subjective. The analysis like this can be used for reducing the data to see better pattern.
### Current Limitation and Future works
It turns out that some of the websites are fake and it is impossible to scrap those websites. The initial analysisi show that the number of left employees are much less than stayed employess that it makes the data biased.In order to pin-point the joint network between all left employees and the pattern of employyes before leaving the company, data need to be analized and shrink down step by step. A lexicon needs to trained based on the technical vocabulary of the companies for finding the polarization of email sentiments. At the end several type of regressor need to be fit and compared for catching the pattern completly. Boosting and bagging needs to be done to overcome to the biased of the data.  






