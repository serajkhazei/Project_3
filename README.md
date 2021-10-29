![bball_bg](./images/bball_bg.jpg)

# Rookie 5 Year Predictions


###  Overview
Project three for Flatiron Data Science BootCamp. In this Project we used various machine learning algorithms to accurately identify NBA rookies that had careers longer than 5 years. We start by importing neccassary packeges, cleaning/exploring the data and building our baseline model. We want to know what in game statitics for players in their rookie year lead to a career longer than 5 years to help our stakeholders get a better understanding on what stats they should focus on for their rookie players. Some of our recomendations include focusing on points per game, games played, rebounds per game, and blocks per game.

### Stakeholder
Our Stakeholders are General managers for various NBA teams.

### Business Problem
Every year NBA teams draft rookies. To predict if those rookies will be successful in the long run can be difficult since so many factors can play a role. Our goal is to limit those factors to just specific in-game stats to aid General Managers in their decision on what to focus on in their rookies.

### Data
We have used two datasets to make our predictive models, 'https://www.kaggle.com/sveneschlbeck/nba-players-career-duration' from Kaggle and 'https://data.world/gmoney/nba-rookies-by-min-1980-2016/workspace/file?filename=NBA+Rookies+by+Year.xlsx' from DataWorld. We concatted both dataset together to get the full array of statistics we were interested in exploring and saved it as nba.csv.

### Methods
We explored the data to see the contents and determine the relevancy of each variable to our Business Problem. Then we ran a heatmap and looked at initial correlation statistics of each variable to career longer than 5 years; our target.

We first created a baseline model and decided to implement a decision tree and used field goal percentage (fg) as our feature. We chose to go with a percentage because statistics like games played, points per game, and minutes per game contain bias.

Then we created train-test split consisting of all the features we decided to keep after our EDA and ran 5 different models which was a Logistic Regression, K-Nearest Neighbors, Decision Tree, Random Forest, and XGBoost. After all those models we then hypertuned the parameters of the logistic regression due the following model giving us the highest accuracy score.

Lastly, to minmize complexity and computational cost we reduced the features down to top 5 features with the highest predictive power, and tested the tuned Logistic Regression with the top 5 features on the tesing set.

### Conclusion 
By using the the features with the greatest predicted odds ratio, the best performing hyper-parameters, and removing excessive features we arrive at a final model that balances high accuracy with reasonable computational costs.

### For More Information
Please review our full analysis in our Jupyter Notebook or our presentation.

### Repository Structure
Describe the structure of your repository and its contents, for example:

├── README.md <- The top-level README for reviewers of this project, you are reading it right now.

├── https://docs.google.com/presentation/d/1Wy7Z5mpkqTLzUsuMDgLRJNFMJk_4zjdAgajiyG8qK5c/edit#slide=id.gfb44c67d90_1_3548 <- PDF version of project presentation

├── code

│ ├── init.py <- .py file that signals to python these folders contain packages

│ └── ipynb_checkpoints.ipynb <- Notebook containing a project checkpoint

├── Dataset <- Both sourced externally and generated from code

└── images <- Both sourced externally and generated from code
