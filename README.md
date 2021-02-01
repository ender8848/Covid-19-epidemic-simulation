# Covid-19-epidemic-simulation
This is my project work for a course taught at University of Rochester called "Numerical Methods and STAT". The project is based on Jupyter Notebook. 

This repository contains a simulation code file based on Jupyter Notebook, an accelerated vedio showing the simulation (you can directly see the video if you do not want to run the code yourself), and us-covid data until April this year. 


The purpose of this project is to use mathematical model to describe Covid-19 epidemic growth in both test and no test condition, and use the model to predict the number of future cases and deaths. The data being used describe the date, cases and deaths of Covid-19 virus from 2020-01-21 to 2020-04-28. All of the data are retrieved from Github[1] and have been verified by The New York Times[2]. 

Firstly, based on the traditional exponential model of epidemic growth, I choose a typical exponential growth period (which starts from 46th day and ends at 60th day) and use non-linear regression to calculate model parameters. After that, I use $R^{2}$ and Shapiro-Wilk test and find out that the model well describe virus growth in that period. Additionally, I try to use exponential model to see what will happen if there is no test and other restrictions on virus

Secondly, I set the 46th day as the initial point and use the parameters in exponential growth model in part1 to deduce relative parameters for Logistic growth model[4].. After that, I try to use the model to fit and predict future growth but only to find very large error, which means the deduced parameters does not work here. In viewing of this, I use non-linear regression to calculate the parameters of Logistic growth model and use the model to predict final confirmed cases in US. Althouth this time the model seems to fit data well mathematically, the predicted final cases may not be precise due to near-linear growth since the 60th day. 

Finally, based on some buildings of University of Rochester and their geographical positions, taking into account the gym, canteen, dorms, and lecturing building, I create a simulation system in which students have both random and orienteering movement during the day in order to simulate the virus spread among students. The whole process are presentated in an animation-like interface. As I did not care much about calculation efficiency, it may takes some time to run the code in part3 and I strongly recommend doing that in localhost.  However, due to the unsolved complicated relationship of the probability of spread in each iteration and real-life infectious rate, this simulation doesn't make a lot of practical sense. You may merely consider this as a game lol!

Reference

1. https://github.com/nytimes/covid-19-data/blob/master/us.csv
2. https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html
3. https://en.wikipedia.org/wiki/Mathematical_modelling_of_infectious_disease
4. http://www.sci.wsu.edu/math/faculty/hudelson/logisticlesson.html
5. https://stackoverflow.com/questions/34486642/what-is-the-currently-correct-way-to-dynamically-update-plots-in-jupyter-ipython

Created: 2021/01

Updated: 2021/01
