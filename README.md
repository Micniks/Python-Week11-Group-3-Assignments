# Gruppe 3 - Uptight Wealth
*Ikke vores valg af gruppenavn*

**Gruppemedlemmer:**
- Cahit
- Marcus
- Michael

# The Python Cult

<img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/bb485920-261e-46b9-896a-cb18fda5d929/dbvl0da-050b7754-242a-4a9f-adff-e4a4c8652fcd.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3sicGF0aCI6IlwvZlwvYmI0ODU5MjAtMjYxZS00NmI5LTg5NmEtY2IxOGZkYTVkOTI5XC9kYnZsMGRhLTA1MGI3NzU0LTI0MmEtNGE5Zi1hZGZmLWU0YTRjODY1MmZjZC5wbmcifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6ZmlsZS5kb3dubG9hZCJdfQ.39OiImVLazb8JFOfhDJWFl2529SJ7obSvPHoSpKNka4" alt="Cult Symbol" width="200">

## Assignment 1: Make a Cultist Model
1. import the data from the dataset, and store it in a pandas variable ***cult***
2. Divide the data into two datasets, ***cultists*** and ***roles***. Make the X dataset for the stats(*features*) of the cultists, by removing the irrelevant data, so you have columns as below, and the Y dataset for the position(*targets*) for the dataset.
```python
['Stealth', 'Influence', 'Endurance', 'Lore', 'Economic', 'Strength', 'Insanity']
```
3. Refactor the dataset ***roles*** so each value become machine friendly numbers, instead of strings.
4. Use LinearRegression to make a model object.
5. Use train_test_split from model_selection, to make training and testing dataset from ***cultists*** and ***roles***
   1. Try adjusting the test_size variable later, to see what gives the better scores.
6. Feed the model with the training datasets, and score the model on the training dataset (*model.score*)
7. Score the model on the testing datasets, and compare to the testing scores.

<img src="http://www.artofmtg.com/wp-content/uploads/2016/03/Cryptolith-Rite-Shadows-over-Innistrad-Art.jpg" alt="Cult Symbol" height="350">

## Assignment 2: Classification of Cultists
*Since the cultist data doesn't seem to have any linear progression, another model might give better result in sorting members...*

1. Use DecisionTreeClassifier to make a new model object
2. Use train_test_split from model_selection again, to make training and testing dataset from ***cultists*** and ***roles***
   1. Try adjusting the test_size variable later, to see what gives the better scores.
3. Feed the model with the training datasets, and score the model on the training dataset (*accuracy _score from sklearn.metrics*)
4. Score the model on the testing datasets, and compare to the testing scores.
5. Compare the scores from using Classification and using Regression models.

*The Score difference is the result of the datasets structure not progressing in a linear fashion, and as such, it is not ideal to use regression for prediction in this dataset.*

<img src="https://i.pinimg.com/564x/02/d8/0a/02d80a719a04e81362bfd0e717cafdb4.jpg" alt="Cult Symbol" height="350">

## Assignment 3: Find Clusters of Cultists
1. Use the orignal dataset again, and remove the charactistic statistics used earlier, as well as the name and position for each member.
2. Remove all rows with missing data for any features
3. Change the Living_Area feature into multiple numeric features, using One Hot Encoding
4. Make a model/analyzer from sklearn.cluster, with the appropriate bandwidth for the data.
   1. **Because the running time for fitting the data is depended on the size of the bandwidth, start out with a max_value of 50 or 100, and increase it in increments, until you think it takes to long to run.**
   2. The higher the bandwidth gets, the longer it takes to run, but you also get fewer clusters in spread.
5. Fit the data into the analyzer
6. Get labels from *analyzer.labels_*, to get the cluster number for each values, and *np.unique* to see how many clusters you have gotten. 
7. Set cluster label into the data for each cultist
8. Make a new dataset, where you group from the people from each cluster together.
9. Adda count feature to each cluster-group, showing how many members are in each cluster
10. Make the dataset from the cluster-array, showing the avarage statistic values for features in each cluster

*The inspiration for this 3rd assignment is from the titanic assignment shown in the material under 11-2*


<img src="https://i.pinimg.com/originals/64/bd/b9/64bdb9f8fea6e1460e816b4bf4cdec8c.jpg" alt="Cult Symbol" height="350">
_______________________

Vi benytter datasættene: [Cultists](https://raw.githubusercontent.com/Micniks/Python-Week11-Group-3-Assignments/main/cultists.csv)

Dette github repository er tilrettet opgavestillinger, så udspecifieret her: [Uge7 Opgave](https://docs.google.com/document/d/1ojSiBWwLo4-Rc7763vx6aVEYdNluATOMja9qqk4dodU/edit#) 
