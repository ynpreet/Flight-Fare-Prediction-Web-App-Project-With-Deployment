<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->


# Flight Price Prediction -A Regression Analysis using Random Forest
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-blue.svg) ![Python 3.6](https://img.shields.io/badge/Python-3.6-brightgreen.svg) ![Scikit-Learn](https://img.shields.io/badge/Library-ScikitLearn-orange.svg)


<details>
  <summary>Table of Contents</summary>
  <ol>
    
* [About The Project](#about-the-project)
* [Motivation](#motivation)
* [Technical Aspect](#technical-aspect)
* [Built With](#built-with)
* [Getting Started](#getting-started)
* [Prerequisites](#prerequisites)
* [Working](#working)
* [Dataset](#dataset)
* [Usage: A Glimpse of Heroku Web app](#usage-a-glimpse-of-heroku-web-app)
* [Deployement on Heroku](#deployement-on-heroku)
* [Roadmap: Directory Tree](#roadmap-directory-tree)
* [Bug / Feature Request](#bug-/-feature-request)
* [Contributing](#contributing)
* [License](#license)
* [And it's done!](#and-it's-done!)
* [Acknowledgments](#acknowledgments)
* [Author](#author)
* [Future Scope](#future-scope)    
  </ol>
</details>

## About The Project

* The objective of this article is to predict flight prices given the various parameters. Data used in this article is publicly available at Kaggle. This will be a regression problem since the target or dependent variable is the price (continuous numeric value).

* Airline companies use complex algorithms to calculate flight prices given various conditions present at that particular time. These methods take financial, marketing, and various social factors into account to predict flight prices.

* Nowadays, the number of people using flights has increased significantly. It is difficult for airlines to maintain prices since prices change dynamically due to different conditions. That???s why we will try to use machine learning to solve this problem. This can help airlines by predicting what prices they can maintain. It can also help customers to predict future flight prices and plan their journey accordingly.

* This particular Airline Flight Fare Prediction project is a Flask web application (deployed on Heroku) to predict airline flight fares across the Indian cities. The dataset for the project is taken from Kaggle, and it is a time-stamped dataset so, while building the model, extensive pre-processing was done on the dataset especially on the date-time columns to finally come up with a ML model which could effectively predict airline fares across various Indian Cities.  
* The dataset had many features which had to pre-processed and transformed into new parameters for a cleaner and simple web application layout to predict the fares. The various independent features in the dataset were: 

  * Airline: The name of the airline.

  * Date_of_Journey: The date of the journey

  * Source: The source from which the service begins.

  * Destination: The destination where the service ends.

  * Route: The route taken by the flight to reach the destination.

  * Dep_Time: The time when the journey starts from the source.

  * Arrival_Time: Time of arrival at the destination.

  * Duration: Total duration of the flight.

  * Total_Stops: Total stops between the source and destination.

  * Additional_Info: Additional information about the flight

  * Price: The price of the ticket

The code is written in Python 3.6.10. 
If you don't have Python installed, you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
pip install -r requirements.txt
```
<p align="right">(<a href="#top">back to top</a>)</p>

## Motivation
People who are travelling in the flights face the problem of price fluctuation to avoid this I thought of to predict the price of the flight ticket so that passenger will have a idea of how much price of flight will be

<p align="right">(<a href="#top">back to top</a>)</p>

## Technical Aspect
* Data collection: [Kaggle dataset](https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh)

* Perfomed exploratory data analysis, feature selection and data modelling: 
  * Perfomed feature selection through (Univariate Selection, Feature Importance & Correlation Matrix with Heatmap)
  * Data modelling using 7 regression models: LinearRegression(), Lasso(), Ridge(), SVR(), RandomForestRegressor(), DecisionTreeRegressor(), xgb.XGBRegressor()
  * Hyperparameter tuning using: GridSearchCV Vs RandomizedSearchCV

* As the model pickle file was greater than 100 MB, I chosed AWS S3 bucket instead of using Git LFS

* I used Sublime sophisticated text editor for coding HTML and flask frame work for for web application development

* Deployed the Flask app on Heroku server

<p align="right">(<a href="#top">back to top</a>)</p>

## Built With

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://scikit-learn.org/stable/_static/scikit-learn-logo-small.png" width=200>](https://scikit-learn.org/stable/)[<img target="_blank" src="https://miro.medium.com/max/1280/1*Mom9A9c2MVqI-V-KPz14ag.png" width=200>](https://s3.console.aws.amazon.com/s3/home?region=us-east-1&region=us-east-1)

<p align="right">(<a href="#top">back to top</a>)</p>

## Getting Started
Welcome to my Getting Started Guide.  Here are some instructions on setting up your project locally:

## ????Prerequisites

```
# import packages
!pip install pyforest
import pyforest
from sklearn.feature_selection import SelectKBest
from sklearn.feature_selection import chi2
from sklearn.ensemble import ExtraTreesRegressor
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.linear_model import Lasso
from sklearn.linear_model import Ridge
from sklearn.svm import SVR
from sklearn.ensemble import RandomForestRegressor
from sklearn.tree import DecisionTreeRegressor
! pip install xgboost
import xgboost as xgb
from sklearn.metrics import r2_score,make_scorer
from sklearn.model_selection import cross_val_score
```
<p align="right">(<a href="#top">back to top</a>)</p>

## ????Working 

Make Sure that you Either Have *Jupyter Notebook* or *Spyder* to Run the code with amazing Visualizations and run any of the following in your Command Prompt in the directory that holds this repo. 

```
Jupyter Notebook
```
or
```
Spyder
```
<p align="right">(<a href="#top">back to top</a>)</p>


## ???? Dataset
You can get the Dataset here

[Link](https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh/)

<p align="right">(<a href="#top">back to top</a>)</p>

## Usage: A Glimpse of Heroku Web app
[Link to Heroku web app](https://airflightfareprediction.herokuapp.com/predict)<br>
![GIF](https://github.com/ynpreet/Flight-Fare-Prediction-Web-App-Project-With-Deployment/blob/main/Repository/Herokuapp/chrome_BuQeKeFIlm.gif)

<p align="right">(<a href="#top">back to top</a>)</p>

## Deployement on Heroku
Login or signup in order to create virtual app. You can either connect your github profile or download ctl to manually to deploy this project.

[![](https://i.imgur.com/dKmlpqX.png)](https://heroku.com)

The next step would be to follow the instruction given in the [Heroku Documentation](https://devcenter.heroku.com/articles/getting-started-with-python) to deploy a web app.

<p align="right">(<a href="#top">back to top</a>)</p>

## Roadmap: Directory Tree 
```
????????? static 
??????? ????????? css
????????? template
??????? ????????? home.html
????????? Procfile
????????? README.md
????????? app.py
????????? flight_price.ipynb
????????? flight_rf.pkl
????????? requirements.txt
```
<p align="right">(<a href="#top">back to top</a>)</p>


## Bug / Feature Request

If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an [issue](https://github.com/ynpreet/Flight-Fare-Prediction-Web-App-Project-With-Deployment/issues) here by including your search query and the expected result
<p align="right">(<a href="#top">back to top</a>)</p>



## Contributing
Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement". Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (```git checkout -b feature/AmazingFeature```)
3. Commit your Changes (```git commit -m 'Add some AmazingFeature' ```)
4. Push to the Branch (```git push origin feature/AmazingFeature ```)
5. Open a Pull Request
<p align="right">(<a href="#top">back to top</a>)</p>



## ????License

This project is licensed under the MIT License - see the [LICENSE.md](https://opensource.org/licenses/MIT) file for details
<p align="right">(<a href="#top">back to top</a>)</p>




## ????And it's done!

- <details> <summary> ???? Problem Solver. Passion Catalyst. Change Maker. Love simulating conversations especially if done over beer. Feel free to contact in case of any query or to collaborate to work on ML projects???? </summary> <a href="https://wa.me/18577019272" target="blank"><img align="center" src="https://github.com/ynpreet/Ynpreet/blob/main/images/5ae21cc526c97415d3213554.png" width="40x" /></a>
</details>
<p align="right">(<a href="#top">back to top</a>)</p>

## ????Acknowledgments

* Special Thanks to **[Amar Mandal](https://www.linkedin.com/in/amar-mandal/)** for sharing wonderful insights about this project
* [Reference](https://www.youtube.com/watch?v=y4EMEpEnElQ) 
* [Reference for Readme.md topics](https://github.com/othneildrew/Best-README-Template/blob/master/README.md)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ## Installing
## Running the tests
## Break down into end to end tests
## And coding style tests
## Deployment
## ????Built With

* [Scikit-learn](https://scikit-learn.org/stable/) 
## Contributing
## Versioning -->


## ????Author

* **Preet Mehta**  
<p>
<a href="https://www.linkedin.com/in/preetmehta/">
  <img align="left" src="https://github.com/ynpreet/Ynpreet/blob/main/images/Linkedin%20(1).svg" alt="kushal's linkedin" width="24px" />
</a>  

<a href="https://ynpreetmehta.medium.com/">
<img align="left" src="https://github.com/ynpreet/Ynpreet/blob/main/images/medium-seeklogo.com.svg" alt="Medium" width="25px" height='23.5' />
</a>  
  
<!-- ![Medium](mediumlogo/medium-seeklogo.com.svg?raw=true "Title") -->
 
<a href="https://www.instagram.com/ynpreet/" target="blank">
  <img align="left" src="https://github.com/ynpreet/Ynpreet/blob/main/images/Instagram%20(1).svg" alt="instagram" width="24px" />
</a>

<a href="https://www.youtube.com/channel/UCCcw6HxUkkfrlKn7-6SszDQ/featured" target="blank">
  <img align="left" src="https://github.com/ynpreet/Ynpreet/blob/main/images/youtube-logo-icon-png-svg.png" alt="youtube"  width="25px" height='23.5' />
</a></p><br><br>
<p align="right">(<a href="#top">back to top</a>)</p>


## Future Scope

* Use multiple Algorithms
* Optimize the performance of Flask app.py
* Front-End development
<p align="right">(<a href="#top">back to top</a>)</p>
