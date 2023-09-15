# dota2predictor
The purpose of this project is to determine and optimize what areas of the game, Dota 2, I should focus on to become a better player by taking personal previous match data and making predictions using machine learning.

The project uses **data analysis** and **data visualization** from various **python libraries** like **pandas**, **matplotlib**to answer the following questions:
  What set of enemy heroes am I best/worst against?
  What set of ally heroes do I play the best/worst with?
  What set of enemy heroes lead to the most/least of my deaths?
  What Heroes do I play best/worst?
  What heroes do I play that have the best/worst networth ?

From this, I can draw patterns to group and classify certain heroes together to determine what styles of play I am best/worst against so that I determine what playstyle should I focus on understanding.

The project utilizes **supervised machine learning** to predict:
 
 Networth 
 Duration of match
 Win probability
 Amount of deaths

Given data of enemy heroes and ally heroes. Determine relationships for each but not together.
  (Ex: Win probability of this match is 50% if I am playing "X" against enemies (1,2,3,4,5)) 
NOT(Ex: Win probability against enemies (1,2,3,4,5) AND allies (6,7,8,9)

The project also utilizes **unsupervised machine learning** to find relationships and patterns to answer:

  When given a subset of enemy heroes, is there some pattern or correlation in:
    The playstyle of the heroes
    What phase of the game the heroes are most impactful (early?mid?late?)
    
  

  
  
  


The project first webscrapes data from past personal match statistics from stratz.com (https://stratz.com/dashboard).
Although initially I tried using selenium to automate webscraping match data, I ended up manually inserting each matches' HTML for my program to run.
