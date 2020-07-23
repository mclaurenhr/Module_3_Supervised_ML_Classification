# Churn Rate Classification Supervised ML (Logistic Regression)

<img src='Pictures\meghan-schiereck-_XFObcM_7KU-unsplash.jpg'/>

## Introduction 
In this project I wanted to solve the business problem of why the phone company SyriaTel is having a customer churn issue. I wanted to predict exactly what the determining factors were for customers to decide to close their accounts. 

I first approached this project by building a pipeline using the models KNN and Decision Trees but after further testing, realized that was not the best modeling choice due to overfitting and inaccurate scores. I then redesigned my ML model and used Logistic Regression to ultimately build my prediction model because I felt that technique was the best one to help solve this business problem.

This project was a very critical learning experience for me because I learned how to be more aware of exactly what process I should be taking and not trying to force a model, technique, or concept on a problem that it will not accurately solve. The "best fit" has two meanings for me at the end of this project, logically and strategically. 

I show the process of how I started off on the wrong path, what made me re-thing my strategy, and what my final predictions were. 

## Data Description
<summary style="font-size: 18px"> Data File Used</summary>

* Churn.csv

## Important Features
The important features that I discovered from my modeling that I used to determine the cause of churn within SyriaTel.

<img src= 'Pictures\Annotation 2020-07-23 133152.png'/>

<details><summary style="font-size: 16px"> Question 1: How does the location of the clients affect churn?</summary>

#### Question Details
I wanted to take a look at the areas, by state, where their were higher and lower total account lengths with customers to determine if the customer location has something to do with the churn rate. What I found was that there were lower account lengths for states who are not typically known to be big business areas and states with below average account lengths accounted for the highest total SyriaTel accounts. 

The states with the highest amount of customers:

1. West Virginia -106
2. Minnesota - 84
3. New York - 83
4. Alabama - 80
5. Wisconsin - 78

This let's me know that there are not enough customers in the states who hold their accounts the longest. Those areas should be SyriaTel's main focus to decrease churn rate as well by increasing account totals in the areas that have to highest client loyalty. 

<img src= 'Pictures\newplot (2).png'/>
</details>

<details><summary style="font-size: 16px"> Question 2: How does the international plan affect the churn rate?</summary>

#### Question Details 
I wanted to look at how SyriaTel's international plan and total international charges affected the customer churn rate. I found that there were higher customer churn with customers who had international plans when their total international charges are 3.5 and higher a month. There is a sweet spot for accounts staying active when the total international charges are between 2 and 3.5 a month. 

<img src= 'Pictures\Annotation 2020-07-10 112202.png'/>
<img src= 'Pictures\Annotation 2020-07-23 083325.png'/>

</details>

<details><summary style="font-size: 16px"> Question 3: Is the International charges priced competitively by minutes enough to keep customers?</summary>

#### Question Details
Lastly, I wanted to look at how total international charge and total international minutes affected customer churn rate. What I found was that there were higher customer churn when the customer used more than 10 minutes a month on their international plan and the average account length used around 7.5 to 13 international minutes a month.

This let me know that the international plans rate is too high for what their customers are willing to pay for. 
<img src= 'Pictures\Annotation 2020-07-23 082401.png'/>
<img src= 'Pictures\Annotation 2020-07-23 083603.png'/>

</details>

## Conclusion/Recommendation

1. I decided to pick the second model because the it had a higher Recall score. Recall was the most important because I was predicting customer churn rates. Recall is called the better safe than sorry metric. I would rather say someone churned when they didn’t and be over precautious verse said they did not churn and they did. They both were not that great but a model having a system with high precision but low recall returns very few results, but most of its predicted labels are correct when compared to the training labels. Verse, a system with high recall but low precision which returns many results, but most of its predicted labels are incorrect when compared to the training labels. I'm looking at the lesser evil between the two. Ultimately you want a system with high precision and high recall which return many results, with all results labeled correctly. Unfortuntely I did not have the ideal model but I might be able to improve my model if I continue to play around with it. 


2. You can tell that my first attempt was not the best and the logistic regression model was definitely the better model. I wanted to show just how important it is to check and reflect on your work to determine if what you built was indeed the best method. Do not be afraid to try something new or to start over all together if you feel you will achieve a better outcome. 

3. For SyriaTel to help minimize their customer churn rate is to re-evaluate their International Plan pricing and options. The customers who are being charged over 3.5 in international charges on their bill a month and using more than 10 minutes in international minutes a month are having very high churn rates. Looking at what other options or offers they can extend to these clients would definitely cut down their churn rate with this group. SyriaTel is probably losing customers to competitors who offer a more affordable International Plan.

4. The areas with below average account lengths also have the highest amount of customers. I think they should refocus on who their target market is to increase poor customer/product fit, watch out for competitors, and conduct a SWOT and marketing analysis. I believe that SyriaTel has a more professional market but an indepth analysis should be done to be sure. 

The Top 3 Important Features were:
1. Total International Charge
2. Area Code
3. Total International Minutes 
4. International Plan
_____
* My confusion matrix work was inspired by Rafael Carrasco, who is my instructor as well! 
<a href="https://github.com/erdosn/good-lessons/blob/master/logistic-regression-and-evaluation-metrics/logistic-regression-notebook.ipynb">Rafael's Github Notebook</a>

* Please check out my blog post as well!
<a href="https://medium.com/@heatherrachael9/confusion-in-the-confusion-matrix-cf7d87494b30">Medium Blog</a>
## Future Work
* I want to look into promotions targeted at the wrong target market. With high users in states where there are low total account lengths lets me know that their customers are being targeted incorrectly. I would want to look more into how they are acquiring these customers to figure out where this disconnect is coming from. 
* SyriaTel has high customer churn rate with their customers with international plans. I want to see what their competitors are offering for their intenational plan customers and see what SyriaTel can do to position or adjust their offers better to retain customers. 
* I also would like to see all of the plan details that SyriaTel offers their clients. It's hard to make a real prediction when a lot of variables are just unknown.   
