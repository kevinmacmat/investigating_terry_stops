# Investigating Terry Stops
This project seeks to investigate Terry Stop data from the Seattle Police Department's Open Data government program from the years 2015 to 2019. Terry Stops derive their origin from the Supreme Court case Terry v. Ohio in which a police officer stopped John Terry on the street, along with two other men, and found two firearms on the men. The officer testified that he used his years of experience as a patrolling officer to judge the mens' reactions which led him to stop them. The Supreme Court ruled that using "probable cause", an officer can stop and frisk a civilian on the street. Using Seattle's Terry Stop data for 28,530 stops I intend to develop an analysis using binary classification to predict whether or not a stop ends in arrest, and to analyze the data in search of any bias when conducting stops and subsequent arrests.

# Exploratory Data Analysis
- 93.5% of stops do not find weapons with 5% finding blades and 1.2% finding firearms.
![](/images/terry_stops_weapons.png)

- Hispanic officers make up the most stops by percentage with 33% while Pacific Islanders have the lowest with 24%
![](/images/terry_stops_by_officer_race.png)

- American Indian and Alaskan Natives are stopped at 5.5 times their population percentage followed by Blacks at 4.81 times their population percentage.
![](/images/terry_stops_by_race.png)
![](/images/terry_stops_pop_by_race.png)

- Police Beats showing the highest number of stops corresponds to Seattle's areas of high displacement risk.
![](/images/terry_stops_beats.png)

# Models and Metrics Used
This analysis used Logistic Regression and Random Forest Classifiers along with gridsearchCV. The metrics used were precision in order to limit false positives, giving officers the benefit of the doubt that no arrest was made, and F1 as a balance between precision and recall in order to paint a more balanced picture. Smote oversampling was used to account for the imbalance in the target variable.

# Conclusion
Although the model itself did not achieve significant predicting power, the analysis was able to highlight a couple areas of potential bias including stops made of Black and American Indian/Alaskan Natives, and a high number of stops made in areas of high displacement risk. 

# Getting Started
To access the project, simply open the mod_2_final_notebook.ipynb file and run the cells in sequential order. The notebook itself has further information explaining the code inside. To view the original csv file along with the cleaned csv files, simply open the folder labeled CSV. This notebook makes use of Scikit Learn, Seaborn, Matplotlib, Stats Models, Numpy, and Pandas packages/modules for its analysis.

Access a powerpoint presentation of the project with the link below: 
https://docs.google.com/presentation/d/1ce0NlisOiCzm4ob58Viq-AZdsL9FkjKfF6AH6S9OZfo/edit?usp=sharing
