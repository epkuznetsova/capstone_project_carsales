# Capstone project: Multi-Objective Optimization Problem on the example of buying a car.

### Project outline:

- Problem statement and assumptions
- Web scraping 
- Data cleaning and preprocessing
- Modelling
- Results visualization

In my Capstone Progect at General Assembly I used Evolutionary Genetic Algorithm (NSGA-II) to solve multiobjective problem.

### Problem statement:
Let's assume that someone is planning to buy a car. Assumption: buyer usually know which car make he or she wants. this assumption was made because most of car makes have its own rate of price decrease (I found it out after scraping data for different car makes). For my analysis I picked most popular car in Australia - Toyota Corolla. The most important features are price, age and odometer (our objectives). 

To understand the problem let's have a look at those four as an example:

![](./pics/table.jpg)


It is unclear which one is the best deal. Because a buyer wants the chipest car with the least odometer and the newest one at the same time. This simple problem is the example multi-objective optimization problem and finding non-dominated solutions.

For this particular case it is required to minimize all the objectives (price, age and odometer). So Pareto-frontier will look like this (in 2D case):
![](./pics/300px-Front_pareto.svg.png)

### Web Scraping:

I collected data for my project by scraping it from web-site www.carsales.com.au. Somehow they didn't block me. Final aquired dataset (before cleaing) was around 4000 cars. I used urllib, requests and Beautiful Soup libraries.

### Data cleaning and preprocessing

Original data set was really messy mainly because all the car make features were placed under one tag:
 
![] (./pics/pastedImage0.png)




