# DATA 505: NFL Salary Judgement

This proejcts explores the expands the topic of sport analytics with financial analysis. We are looking into wehther NFL players are being **underpaid**,**overpaid**, or **paid fairly** relative to their on-field preformance. We are doing this with the usage of machine learning classification mdels, that we are enginnering for position specific archetype features and team-level salary cap allocations metrics 

This project will completeted as a final project for **DATA 505: Applied Machine Learning** at Willamette Univeristy (Spring 2026).

Team Members:
* Haydn Duncan
* Dylan Ray
* Brandon Smith
* Jackson Garro
___________________
# Research Question
* **RQ1:** Does classifying players into position-specific archetypes (e.g, power back vs. receiving back) improve the model's ability to predict whether a player is underapid, overpaid, or fairly paid - and which archetypes show the most consistent market mispricing?

* **Hypothesis 1:** We are hypothesize that archetype-based features will outperform broad position labels because salary value in the NFL is determined relative to a player's specific role, not just their position group. A model that is specically made/understands *what kind* of player they are will be able to create a more accutrate pay classifcation than a generalized one. For example, we are not going to compare Christian Mccaffrey's contract vs Derrick Henery's. They are two completely different players and their skill set is drastically different. This does not make one better than the other if we are not solely looking at their stats, but it depends on how much that team's value their position-specific archetype/skill set. 

---------------
* **RQ2:** Does a team's proportional salary cap spending at a given position influence whether playes at that position are classified as overpaid relative to their perforamnce output?

* **Hypothesis 2:** Every NFL team must follow a strict hard salary cap (303.5 million per team; via *overthecap.com/salary-cap-space*).This puts pressure of the team's management to allocate the proper/respectable amount for each position group. We hypothesize that players on teams with above-average cap investment at their position will be more liekly to be classified as overpaid, because heavy positional spending will inflate individuals salaries beyond their on-field performance statistics alone would justify. 


_______________
# Data Sources
Performance Data - nflreadpy (nflverse)
  * **Library:** nflreadpy - Python port of the nflreadr R package
  * **Data Pulled:** Player-leel seasonal perofrmance statistics, snap counts, and Next Gen Stats

Financial Data - Kaggle
  * **Dataset:** https://www.kaggle.com/datasets/marcothompson/nfl-player-list-w-attributes-salaries
  * **Format:** 1 CSV file containing player attributes and salary information. 

------------
# Models
| Model | Role |
|---|---|
| Logistic Regression | Baseline |
| K-Nearest Neighbors (KNN) | Distance-based; tuned via cross-validation |
| Random Forest Classifier | Primary model; feature importance output |

____________
# Key Concepts for Context
* **Salary Cap:** The Nfl efnoreces a hard annual spending limited (it grows over the years and projected to be 350+ million by 2028). Every player contracts count against their cap, creating a real financial trade off for their front offices.
* **Free Agency:** Players with expiring contracts enter the open market where teams bid on their services. The primary goal is that their contracts will inflate and correct relative to their last seasons performance.
* **Pay Fairness Label:** Derived from teh Kaggle dataset, this label classifies each player as underpaid, overpaid, or fairly paid based on the relationship between their salary and their on-field performance.

------------
# Potential Stakeholders
* NFL front offices and General Managers
* Sport agents
* Fantasy football analysts
* Sports finance researchers
