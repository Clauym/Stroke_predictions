![cover](/Images/dataset-cover.jpg)
# Brain Stroke Predictions

### Rationale
A ischemic stroke (or cerebrovascular accident) occurs when the blood supply to a part of the brain is interrupted o reduced. In accordance to the Natinal Center for Health it is the fifth cause of dead for people in the US with an account of 162,890 people during 2021. Globally strokes are the second cause of death globally. These factors make the study of strokes an interesting one in an era where we can make use of recent technologies in order to estimate, and hopefully reduce, this kind of incidents.

### Questions:
1. How gender affects brain stroke deaths?
2. Are there noticeable different factors between the people dead by brain stroke and those who do not?
3. Is there a model that estimates the outcomes better (we will test 2 models at least)?
4. At what age are people having the highest probability of a brain stroke in this dataset?
5. Are there any factors that better predict increased risk of brain stroke?

You can preview the brain stroke data set (.csv) used on this project [HERE](/Resources/brain_stroke_data.csv). To download the original data set click [HERE](https://www.kaggle.com/datasets/zzettrkalpakbal/full-filled-brain-stroke-dataset/download?datasetVersionNumber=2).
https://www.kaggle.com/datasets/zzettrkalpakbal/full-filled-brain-stroke-dataset

### Members: 
* Jay Laxami - [Github](https://github.com/JayLaxami)
* Will Macmillan - [Github](https://github.com/willmacmillan)
* Candida Miranda - [Github](https://github.com/candidamg)
* Claudia Yurrita - [Github](https://github.com/Clauym)


## License & Images

<b> License </b><br>
[CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/)

<b> Cover </b><br>
Note: this cover has been cropped from the original size. Image Credit: [Piyaphat_Detbun/Shutterstock.com](Piyaphat_Detbun/Shutterstock.com). You may find the source [here](https://www.news-medical.net/news/20211117/Raising-awareness-of-stroke-and-how-to-prevent-it.aspx).

## Dataset
The dataset was found in Kaggle under the following link: 
<https://www.kaggle.com/datasets/zzettrkalpakbal/full-filled-brain-stroke-dataset><br>
It consists of 10 different features related to strokes.
The variables are:
Age,
Bmi,
Average glucose level,
Gender -Male or Female,
Hypertension -Yes or no,
Heart disease -Yes or no,
Ever married - Yes or no,
Residence type -Urban or Rural,
Smoking status - smoker, former smoker, never smoked, unknown,
Work type - Children, Government job, Never worked, Private or Self-employed

## Scope of the project
Our goal is to find an accurate model that can predict strokes on the population given in the database we chose.
## Development
The dataset source was in a csv format where it was cleaned and loaded into a PostgreSql database.
### Manipulation of the data
a. Due to the many disparities between the values of the explanatory variables, we standarized the data for every model.
b. The categorical variables with two outcomes were transformed into numbers.
c. The categorical features with three or more possible outcomes were substituted with dummies.
d. We ran a correlation matrix in order to avoid possible multicollinearity in the model.
e. After running the models we tried to correct the unbalance in the dataset by oversampling all the models.
### Model results
1. REGRESSION MODEL
   - Total accuracy: 0.50.
   - Precision of stroke predictions: 1.0
   - Recall of strokes predictions: 0.01 <br>
   
*Oversampled*
   - Total accuracy: 0.78.
   - Precision of stroke predictions: 0.16
   - Recall of strokes predictions: 0.82
2. DECISION TREE MODEL
   - Total accuracy: 0.91.
   - Precision of stroke predictions: 0.15
   - Recall of strokes predictions: 0.16 <br>
   
*Oversampled*
   - Total accuracy: 1.00.
   - Precision of stroke predictions: 1.00
   - Recall of strokes predictions: 1.00<br>
3. RANDOM FOREST MODEL
   - Total accuracy: 0.95.
   - Precision of stroke predictions: 0.00
   - Recall of strokes predictions: 0.00 <br>
   
*Oversampled*
   - Total accuracy: 1.00.
   - Precision of stroke predictions: 1.00
   - Recall of strokes predictions: 1.00<br>
   
4. NEURAL NETWORK MODEL
   - Total accuracy: 0.94.
    
We progressed through the various models because the first models ran did not produce accuracy results sufficient to our liking. We also saw the Decision Tree and Random Forest models were the best ones after oversampling them.

### Visualization of data
As a final point we created some visuals in a Tableau Dashboard.
