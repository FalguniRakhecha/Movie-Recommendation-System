# Movie-Recommendation-System

I built this recommendation system using DBSCAN algorithm. You can refer to the dataset using the below link. The dataset include data for the movies from Netflix, amazon prime and HBO max TV. 
https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies?datasetId=2178661&sortBy=voteCount
https://www.kaggle.com/datasets/victorsoeiro/hbo-max-tv-shows-and-movies?select=titles.csv
https://www.kaggle.com/datasets/victorsoeiro/amazon-prime-tv-shows-and-movies?select=titles.csv

In the begenning I have imported necessery files and data into my notebook. Starting with data cleaning and preprocessing.
I removed unnecessary and duplicate columns from the dataset. Their were some columns which needed some preprocessing, like production countries column had the data stored in brackets and some comma. Also some row had multiple values and some had no values. Preprocessing this data I created a new column with modified format. 
Once the data preprocessing was done I have encoded the features i.e. column values are converted from string to integer format. 
After data was ready for preprocessing, DBSCAN algorithm is applied. 

## DBSCAN
I initialized 2 array with some values and now we choose best epsilon and minpoint values. Iterate over each combination of these values and calculate silhoutte score for each combination. The combination of values of epsilon and minpoint which give maximum silhoutte score is choosen as hyper parameters.
Applying DBSCAN algorith we create clusters and save them in new column.
Now create a function that will take movie name as parameter and match it with other movies. If the cluster value for both the movies match each other, put then together and return the result. 


