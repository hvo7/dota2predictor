# Dota2Predictor

The purpose of this project is to determine and optimize what areas of the game, Dota 2, I should focus on to become a better player by taking personal previous match data and making predictions using machine learning.

## Table of Contents
- [Introduction](#introduction)
- [Questions Answered](#questions-answered)
- [Machine Learning](#machine-learning)
- [Data Collection](#data-collection)

## Introduction

### Motivation
This project focuses on predicting the outcome of Dota 2 matches based on hero compositions using neural networks and machine learning. A brief description on the premise of Dota 2 can be found from the link below

- https://dota2.fandom.com/wiki/Dota_2

Given the numerous complexities and concepts in the game, it can be challenging for players to pinpoint their weaknesses. To address this, I developed a prediction model to analyze playstyles and identify the types of heroes a player struggles against.

I use **data analysis** and **data visualization** from various **Python libraries** like **pandas** and **matplotlib** to answer the following questions:

- What set of enemy heroes am I best/worst against?
- What set of ally heroes do I play the best/worst with?
- What set of enemy heroes lead to the most/least of my deaths?
- What Heroes do I play best/worst?
- What heroes do I play that have the best/worst net worth?

## Extracting Data

I use the **Selenium** and **BeautifulSoup** packages alomg with **Pandas** to extract data of my personal matches recorded by Stratz.com (https://stratz.com/dashboard).
I extracted features such as Win result (Win or Loss), Hero (The Hero I played), and Enemy/Ally Heroes (Positions 1-5 of all heroes in the game).

## Data Analysis

I cleaned the data to analyze more efficiently.
I use **matplotlib** to plot variables and examine possible trends within the data.

Used **Matplotlib** to analyze and create graphs of various columns.
 - Analyzed Kills, Deaths, Assists vs. Hero for all positions 1-5
 - Also analyzed average KDA for each of heroes I played
     - Constraint: Hero must have been played with/against >5 matches.
## Prediction

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
Used **Binary Logitical Regression** with **Scikit-Learn** to predict win probability vs the following:
 - Deaths
 - Kills
 - Assists
 - Networth



