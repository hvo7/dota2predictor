# Dota2Predictor

The purpose of this project is to determine and optimize what areas of the game, Dota 2, I should focus on to become a better player by taking personal previous match data and making predictions using machine learning.

## Table of Contents
- [Introduction](#introduction)
- [Questions Answered](#questions-answered)
- [Machine Learning](#machine-learning)
- [Data Collection](#data-collection)

## Introduction

The project uses **data analysis** and **data visualization** from various **Python libraries** like **pandas** and **matplotlib** to answer the following questions:

- What set of enemy heroes am I best/worst against?
- What set of ally heroes do I play the best/worst with?
- What set of enemy heroes lead to the most/least of my deaths?
- What Heroes do I play best/worst?
- What heroes do I play that have the best/worst net worth?

From this, I can draw patterns to group and classify certain heroes together to determine what styles of play I am best/worst against so that I determine what playstyle should I focus on understanding.

## Questions to answer

The project utilizes **supervised machine learning** to predict:

- Net worth
- Duration of match
- Win probability
- Amount of deaths

Given data of enemy heroes and ally heroes, it determines relationships for each but not together.

- (Ex: Win probability of this match is 50% if I am playing "X" against enemies (1,2,3,4,5))

It does NOT consider combinations like:

- (Ex: Win probability against enemies (1,2,3,4,5) AND allies (6,7,8,9))

The project also utilizes **unsupervised machine learning** to find relationships and patterns to answer:

- When given a subset of enemy heroes, is there some pattern or correlation in:
  - The playstyle of the heroes
  - What phase of the game the heroes are most impactful (early? mid? late?)

## Machine Learning


## Data Collection

The project first web scrapes data from past personal match statistics from [stratz.com](https://stratz.com/dashboard). The automatic_webscraper program creates a dataframe then launches the matches page and filters by Hard Support and Ranked matches. The program then opens each match in a new tab and copies the HTML to a txt file. The scraper program then take the data and adds it to the dataframe. This process is repeated for each match automatically and will take approximately 30-40 min to complete all 401 matches. 
