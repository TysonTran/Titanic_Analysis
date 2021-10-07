# Titanic Analysis
This is a exploratory data analysis of the titanic dataset from Kaggle with a ML model. I was exploring the data to gain insight on what caused individuals to have a better chance of survival and created a ML model to predict who would survive and who wouldn't.

## Findings

### Survival of Males Versus Females on the Titanic?
* 64.8% (577) males on the ship and 35.2% (314) females
* Only 18.9% (109) of males survived while 74.2% (233) of females survived

### Ticket Class Affect Survival?
* 24.2% (216) of Passengers in First Class, 20.7% (184) of Passengers in Second Class, and 55.1% (491) of Passengers in Third Class
* 63% (136) of First Class Passengers Survived, 47.3% (87) of Second Class Passengers Survived, and 24.2% (119) of Third Class Passebgers Survived

### Port of Embarkation Affect Survival?
* 72.5% (646) of Passengers boarded at Southampton, 18.8% (168) of Passengers boarded at Cherbourg, and 8.6% (77) Passengers boarded at Queenstown
* The majority that boarded at Cherbourg was first class while Southampton and Queenstown was third class
* Cherbourg had the highest rate of survival at 55.4% (93), then Queenstown at 39% (30), then Southampton at 33.9% (219)

### Family Affect Survival?
* Most common family size on the ship was 1 which was just the individual by themself.
* Rate of Survival was highest where the family size was 4 with a 72.4% chance of survival

### Ages Affect Survival?
* When splitting the ages into decades, we noticed that the only age group that had more survive than die was those between 0-10

### ML Model
* Looking to predict if a person on the titanic will survive
* Features Used: Pclass, Sex, Embarked, Fam, Decade
* Used the supervised learning algorithm K Nearest Neighbors to predict of an individual would survive because the algorithm looks for training examples that are close to make a prediction
* Received a accuracy score of .798
* Improved the algorithm with a grid search to find the optimal parameters. Fount that the optimal parameters were metric='manhattan', n_neighbors=13, and weights='uniform
* Improved model by .013
* Used K-Fold Cross Validation to look for over or underfitting. Did not notice it over or underfitting.
