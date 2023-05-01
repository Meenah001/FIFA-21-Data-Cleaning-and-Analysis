# FIFA-21-Data-Cleaning-and-Analysis

The project is all about data cleaning, which is the crucial step in analysis.

---

# INTRODUCTION

Data cleaning is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset. When combining multiple data sources, there are many opportunities for data to be duplicated or mislabeled. If data is incorrect, outcomes are unreliable, even though they may look correct. There is no one absolute way to prescribe the exact steps in the data cleaning process because the processes will vary from dataset to dataset. But it is crucial to establish a template for your data cleaning process so you know you are doing it the right way every time. The following are some of the things to look for while cleaning a data;

. Remove duplicate entries

. Fix structural errors (errors in spelling and values)

. Get rid of unnecessary spacing in the dataset

. Handle missing data

. Change data type where necessary

. Filter unwanted outliers

. Remove irrelevant data

---

# ABOUT THE DATASET

The dataset used for this challenge is the FIFA 21 data. It was sourced from Kaggle. Here is the link to access it https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring . It contains the details of football players with their performance which was updated up till 2021. There are 18980 rows (this includes the headers) and 77 columns present in the FIFA 21 data. The dataset contains the following information: ID, Name, Full Name, Photo Url, Player Url, Nationality, Age, Overall Rating, Potential Rating, Club, Contract Start, Contract End, Positions, Best Position, Preferred Foot, Height, Weight, BOV, Joined, Loan Date End, Value, Wage, Release Clause, Attacking, Crossing, Finishing, Heading Accuracy, Short Passing, Volleys, Skill, Dribbling, Curve, FK, Accuracy, Long Passing, Ball Control, Movement, Acceleration, Sprint, Speed, Agility, Reactions, Balance, Power, Shot Power, Jumping, Stamina, Strength, Long Shots, Mentality, Aggression, Interceptions, Positioning, Vision, Penalties, Composure, Defending, Marking, Standing Tackle, Sliding Tackle, Goalkeeping, GK Diving, GK Handling, GK Kicking, GK Positioning, GK Reflexes, Total Stats, Base Stats, Weak Foot Ability, Skill Moves, Ability, Attacking Workrate, Defensive Workrate, IR, Pace, SHO, PAS, DRI, DEF, PHY, Hits. All these are the variables that contain all the data.

---

# THE DATA DICTIONARY

Here is a brief documentation for each column name in the given dataset:

photoUrl: The URL of the player’s photo.

LongName: The full name of the player.

playerUrl: The URL of the player’s page on sofifa.com.

Nationality: The nationality of the player.

Positions: The positions the player can play.

Name: The short name of the player.

Age: The age of the player.

OVA: The overall rating of the player in FIFA 21.

POT: The potential rating of the player in FIFA 21.

Team & Contract: The team the player is playing for in FIFA 21, along with their contract details.

ID: The unique identifier for the player.

Height: The height of the player in feet and inches.

Weight: The weight of the player in pounds.

foot: The preferred foot of the player.

BOV: The best overall rating the player has achieved in their career.

BP: The best position the player has played in their career.

Growth: The difference between the potential rating and overall rating of the player.

Joined: The date the player joined their current team in FIFA 21.

Loan Date End: The date the player’s loan contract ends.

Value: The market value of the player in FIFA 21.

Wage: The weekly wage of the player in FIFA 21.

Release Clause: The release clause value of the player in FIFA 21.

Attacking: The attacking attributes of the player.

Crossing: The crossing attribute of the player.

Finishing: The finishing attribute of the player.

Heading Accuracy: The heading accuracy attribute of the player.

Short Passing: The short passing attribute of the player.

Volleys: The volleys attribute of the player.

Skill: The skill attributes of the player.

Dribbling: The dribbling attribute of the player.

Curve: The curve attribute of the player.

FK Accuracy: The free kick accuracy attribute of the player.

Long Passing: The long passing attribute of the player.

Ball Control: The ball control attribute of the player.

Movement: The movement attributes of the player.

Acceleration: The acceleration attribute of the player.

Sprint Speed: The sprint speed attribute of the player.

Agility: The agility attribute of the player.

Reactions: The reactions attribute of the player.

Balance: The balance attribute of the player.

Power: The power attributes of the player.

Shot Power: The shot power attribute of the player.

Jumping: The jumping attribute of the player.

Stamina: The stamina attribute of the player.

Strength: The strength attribute of the player.

Long Shots: The long shots attribute of the player.

Mentality: The mentality attributes of the player.

Aggression: The aggression attribute of the player.

Interceptions: The interceptions attribute of the player.

Positioning: The positioning attribute of the player.

Vision: The vision attribute of the player.

Penalties: The penalties attribute of the player.

Composure: The composure attribute of the player.

Defending: The defending attributes of the player.

Marking: The marking attribute of the player.

Standing Tackle: The standing tackle attribute of the player.

Sliding Tackle: The sliding tackle attribute of the player.

Goalkeeping: The goalkeeping attributes of the player.

GK Diving: The goalkeeper diving attribute of the player.

GK Handling: The goalkeeper handling attribute of the player.

GK Kicking: The goalkeeper kicking attribute of the player.

GK Positioning: The goalkeeper positioning attribute of the player.

GK Reflexes: This refers to the goalkeeper’s ability to react and make saves quickly.

Total Stats: This refers to the overall rating of the player based on their performance in all areas of the game.

Base Stats: This refers to the player’s rating in the six main areas of the game: Pace, Shooting, Passing, Dribbling, Defending, and Physicality.

W/F: This refers to the player’s weaker foot ability.

SM: This refers to the player’s skill moves ability.

A/W: This refers to the player’s attacking work rate. It measures how frequently the player participates in attacking actions, such as making runs or positioning themselves in the opponent’s half.

D/W: This refers to the player’s defensive work rate. It measures how frequently the player participates in defensive actions, such as tracking back or making tackles.

IR: This refers to the player’s injury resistance. It measures the player’s ability to avoid injuries and how quickly they recover from them.

PAC: This refers to the player’s pace or speed attribute. It measures how quickly the player can move with and without the ball.

SHO: This refers to the player’s shooting ability. It measures the player’s accuracy and power when shooting the ball.

PAS: This refers to the player’s passing ability. It measures the player’s accuracy and range when passing the ball.

DRI: This refers to the player’s dribbling ability. It measures the player’s agility, balance, and ball control when dribbling the ball.

DEF: This refers to the player’s defensive ability. It measures the player’s ability to tackle, intercept, and defend against opposing players.

PHY: This refers to the player’s physicality or strength. It measures the player’s ability to win physical battles and maintain possession of the ball.

Hits: This refers to the number of times the player’s profile has been viewed on the website.

---

# STEP BY STEP PROCESS IN CLEANING THE DATA

![dc](https://user-images.githubusercontent.com/97677904/235482238-26a97d67-4639-4ef1-987e-d99097c45bbf.jpg)

First of, the data in it raw form was originally downloaded as a zipped file which was then extracted and changed to CSV (comma separated values) format. This was then loaded to Microsoft Excel. The image below shows the dataset in it raw form when loaded to Excel.

![RAW DATA](https://user-images.githubusercontent.com/97677904/235483023-4a64cee5-e6c0-4747-aa0b-ac6b6696416b.jpg)

Note: Before going further with your cleaning, make sure you have a backup of your data. This would save you in a case where the original data has some errors that needs correction.

After loading the data to the power query editor in Microsoft Excel, I noticed that almost all the records in the column has some extra spaces in between them. While going through to see where the problem came from, I got to know it was from a column named “Club” which has all it records written at the bottom instead of it being at the upper part of the line.









































