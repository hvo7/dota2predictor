# dota2predictor
The purpose of this project is to determine and optimize what areas of the game, Dota 2, I should focus on to become a better player.


The project uses **data analysis** and **data visualization** to answer the following questions:
  What set of enemy heroes am I best/worst against?
  What set of enemy heroes lead to the most/least of my deaths?
  What set of ally heroes do I play the best/worst with?
  What Heroes do I play best/worst?

From this, I can draw patterns to group and classify certain heroes together to determine what styles of play I am best/worst against so that I determine what playstyle should I focus on understanding.


Also, the project utilizes **machine learning** to determine:
  What is my win probability if I were to choose hero X, given a set of enemy heroes?
    What if I were given a set of ally heroes?
    

The project first webscrapes data from past personal match statistics from stratz.com (https://stratz.com/dashboard).
Although initially I tried using selenium to automate webscraping match data, I ended up manually inserting each matches' HTML for my program to run.
