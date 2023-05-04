# FIFA-21-Data-Cleaning-and-Analysis

The project is all about cleaning and analysing the dataset to get some meaningful insight from it.

![Screenshot 2023-05-01 142703](https://user-images.githubusercontent.com/97677904/235506580-a987b861-9c8f-4ce4-b80c-025e80d1fa6a.jpg)

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

# Below is the image of how the data looks like before the removal of the excess spaces

![1 excess space](https://user-images.githubusercontent.com/97677904/235484353-f36833b5-9c08-4d56-9a27-bc4e10bf7d1b.jpg)

In order to remove the excess spaces, I selected the club column which is obviously the one causing the excess spaces. I then right-click on it, this popped up different options. I clicked on TRANSFORM in the available options and then select TRIM, this helped to remove the excess spaces. The image below shows the data after the excess spaces have been removed.

![2 excess space trimmed](https://user-images.githubusercontent.com/97677904/235485237-f9b0f562-ef3e-434e-bbb2-4bdb6fc3b7dc.jpg)

---

After removing the excess spaces from the data, I started the cleaning process from the first column which was the “ID” to the “Hits” column which was the last column in the dataset. Follow as I show you the step by step guides to clean all the dirty records in the data.

ID: This is the unique identifier of each record in the Table. I noticed that the data type used was wrong (Whole number data type) and I changed it to the appropriate data type (Text data type)

![Id](https://user-images.githubusercontent.com/97677904/235485884-7fb1e3a6-af7a-48ee-b826-66b1c939c8ed.jpg)                  ![id change](https://user-images.githubusercontent.com/97677904/235486006-edca3e27-d598-4e30-857b-125ade38b9dc.jpg)

---

Name: In this column a special character was found. In order to remove this, I replaced the special character with correct letter.

![spc](https://user-images.githubusercontent.com/97677904/235486848-0eeca1a6-e2e1-44f3-8544-d87bb9441350.jpg)


Note: Always filter your data to check if the records in each column contains any forms of error such as spelling mistakes, special characters, null values, outliers among others

---

Photo URL and Player URL: These two columns were removed. This is because they are both meta-data (meta-data describes and gives information about another data).

![meta](https://user-images.githubusercontent.com/97677904/235487149-4203672d-7e41-4f01-be88-9fddcb91655c.jpg)

---

Nationality, Age and Club: No cleaning was needed in these three columns, because they had no issues of missing values, null values or data type problems.

![3](https://user-images.githubusercontent.com/97677904/235489519-85cf49a9-9589-47a7-a06d-c2a47078e78a.jpg)

---

OVA and POT: According to the data dictionary, it was made known that OVA means the player Overall Rating and POT means Overall Potential. These two columns were to be measured in percentage. To do that I divided both column by 100, I then changed both data type to % and also the column name from OVA/POT to their full meaning has given in the data dictionary.

# BEFORE
![5 OVA column was to change to percentage](https://user-images.githubusercontent.com/97677904/235492044-0bb95aef-879f-46db-a913-fb38c704173d.jpg)

# AFTER
![8 POT changed to potntial rating   %](https://user-images.githubusercontent.com/97677904/235492373-882ca19b-4123-40a7-b149-94b2fea680a8.jpg)

---

Contract: This column has a lot of work to be done on it, and this is because it contains some inconsistent values in the record. It represents the players “Start” and “End” of contract in years, but it was seen that some the players contracts were PAID, some were LOAN while others were FREE.

![cont](https://user-images.githubusercontent.com/97677904/235492757-e2301795-7429-494b-9a02-6d2daa9ebf2b.jpg)

A conditional column was created in order to group the different types of contracts (i.e Contracts, Loan and Free) in a separate column.

![10 conditional formatting 4 contract column](https://user-images.githubusercontent.com/97677904/235493064-96a8b0e0-c149-431f-a571-23c1bf32223c.jpg)

After applying the conditional column, the below column was created ( Agreement column).

![11 Result of conditional column](https://user-images.githubusercontent.com/97677904/235493191-0bdd0d12-1d89-4aa6-b5a1-1350f0565588.jpg)

After getting the new column i.e the “Agreement column” , I split the contract column by delimiter which was the (~) sign between each contract year so as to get the contract starting year and End year. This gave two new columns namely contract.1 and contract.2

![12 contract column splitted to get the start and end year of contract](https://user-images.githubusercontent.com/97677904/235493381-6fa3e3e8-9d6a-4d2d-8bba-e6550d04a78d.jpg)

Further analysis was made to get the duration of each contract, this was done by using the Custom Column under the Add Column ribbon. Then the below formula was input in it i.e subtracting the Contract.2 from Contract.1 Some empty values were returned after the operation was carried out, and they were all replaced with null.

![13i contract duration got using custom column 2 subtract strart 4rm end](https://user-images.githubusercontent.com/97677904/235493714-13ca8e71-eb87-4696-a96b-d09cc832501d.jpg)

---

Height: This column shows the height of each player. There were some inconsistency in the value recorded under this column. some heights were measured in cm while some in feet and inches.

![13 Hight colum in cm,lbs $ inches](https://user-images.githubusercontent.com/97677904/235494460-fc4c6f0e-9ba1-4c9e-841b-5529f1436588.jpg)


Three tasks are needed to be carried out here. Firstly, convert foot to inches, secondly to convert inches to cm and lastly to convert foot to cm . The below formula was used.

12 inches = 1ft

0.393701 inch = 1cm

Formula for inches

foot * 12 + inches

Using conditional column, I converted the foot to inches by multiplying the foot by 12 , also converted the inches to cm using 0.393701 by applying conditional statement. I then split the column by delimiter to separate the feet from inches. After which I then added the inches which was separated with the feet in order to convert to inches. The final task was to divide the result gotten from conversion to inches by 0.393701 which result in converting all the records to cm.

![14 conditional column 2 convert 2 cm](https://user-images.githubusercontent.com/97677904/235494591-76965a0e-b8dd-456f-be19-f69383c46102.jpg)

![15 the height column was split by ' delimeter ](https://user-images.githubusercontent.com/97677904/235494638-3f077d98-3aa8-407e-8710-7f73b3f4d0fa.jpg)

![16 cleaned height column](https://user-images.githubusercontent.com/97677904/235494713-f23db83d-3a68-4b17-a42c-fb4f78a0d1de.jpg)

---

Weight: Similar problem has “Height” was faced here, some of the records were measured in kg and lbs. I applied the same process used in the Height column too, but a different conditional statement was used for the conversion since we’re converting from “kg” to “lbs.” as stated in the data dictionary. So, I converted the records from “kg” to “lbs.” using this formula 2.205kg = 1lbs.

![17 weight col contains diff unit](https://user-images.githubusercontent.com/97677904/235495089-75441aa3-a03b-49a5-ad56-1fe3563ce1dd.jpg)

![18i weight conversion using conditional col (lbs)](https://user-images.githubusercontent.com/97677904/235495137-b3b1b6ac-527a-4cd6-8dcd-22c9dc05e62a.jpg)

![19 weight cleaned](https://user-images.githubusercontent.com/97677904/235495176-05359c36-49cb-4c26-bf0b-b1fb1a8566a7.jpg)

---

Joined: I filtered this column to check for any inconsistencies in the record, there were no inconsistent records found. The data type used was appropriate.

![joined](https://user-images.githubusercontent.com/97677904/235495469-e09a4356-72e8-4962-bad7-47a427b2577c.jpg)

---

The Value, Wage, and Release-Clause: This represents the market value, weekly wage and release clause of players in FIFA 2021. I noticed some of the records have K while others have M so we need to convert them to currency, so I multiplied the M values with 1,000,000 and the K values with 1,000 by using conditional statement. So, I removed the “M”,”K”, and “€” in order to multiply the column with the Conditional Column Created.

![20 Value col with inconsitent unit (M   K)](https://user-images.githubusercontent.com/97677904/235495770-7e415659-1be5-48bf-9066-76c22f734200.jpg)

![25 wage col cleaned](https://user-images.githubusercontent.com/97677904/235496042-024df4dc-152c-4cc9-9176-cadc77e5fa4f.jpg)

![27 release col cleaned](https://user-images.githubusercontent.com/97677904/235496129-27582b1d-70ff-4260-b599-cb1ab637efde.jpg)

---

W/F, S/M and IR: They’re measured in the scale of 1–5. I removed the star rating by using the replace value and changed the datatype to whole number.

![28 d selected cols has star @ d back of their values](https://user-images.githubusercontent.com/97677904/235496315-d5612f4e-778a-45f8-8533-e39392b48325.jpg)

![29 replac val funtx used to rmove d star](https://user-images.githubusercontent.com/97677904/235496355-0b26e2a9-d195-4fa5-a991-2a91e7a6608f.jpg)

---

Attacking’, ‘Crossing’, ‘Finishing’, ‘Heading_accuracy’, ‘Short_passing’, ‘Volleys’, ‘Skill’, ‘Dribbling’, ‘Curve’, ‘FK_accuracy’, ‘Long_passing’, ‘Ball_control’, ‘Movement’, ‘Acceleration’, ‘Spring_speed’, ‘Agility’, ‘Reactions’, ‘Balance’, ‘Power’, ‘Shot_power’, ‘Jumping’, ‘Stamina’, ‘Strength’, ‘Long_shot’, ‘Mentality’, ‘Aggression’, ‘Interception’, ‘Positioning’, ‘Vision’, ‘Penalties’, ‘Composure’, ‘Defending’, ‘Marking’, ‘Standing_tackle’, ‘Sliding_tackle’, ‘Goalkeeping’, ‘GK_handling’, ‘GK_diving’, ‘Gk_kicking’, ‘Gk_positioning’, ‘Gk_reflexes’, ‘Total_stats’, ‘Base_stats’, ‘Pace’, ‘Shooting’, ‘Passing’, ‘DRI’, ‘DEF’, ‘Physical’, ‘Best_position’, ‘Preferred_foot’, ‘Attacking_workrate’, and ‘Defensive_workrate’: These columns were checked and no issues found within the data. The data types were also checked, and changes were made for some that had wrong data types and column names corrected.

![agiki](https://user-images.githubusercontent.com/97677904/235496947-156f1f09-9723-4638-93d2-c34ad4c17a40.jpg)

---

Hit: This refers to the number of times a player’s profile has been viewed on the website. The column has some blanks which means the players has no hit which was replaced with zero. Some players has over a thousands view which is represented by “K” which was removed and multiply by 1000 using Conditional Column.

![30 Hits col has valus dat has K ](https://user-images.githubusercontent.com/97677904/235497013-95617d14-f29d-4329-906a-a225626ce076.jpg)

![31 condtn col was used 2 remove K in Hits col](https://user-images.githubusercontent.com/97677904/235497106-c6dbde55-bd01-4978-b5da-f55e3f4ddeda.jpg)

![32 Hit col cleaned](https://user-images.githubusercontent.com/97677904/235497148-090493c4-99e5-44ff-9162-4906946576ff.jpg)

---

After all the cleaning has been done, the data was loaded to Microsoft Excel using the “Close & Load” option on the top left section of the Power Query Editor.

Below is the cleaned dataset on Microsoft Excel after all the cleaning and transformations.

![cleaned](https://user-images.githubusercontent.com/97677904/235503430-ff5c1c1e-c3ba-4eab-b377-6d028f2a2ca6.jpg)

---

# PROBLEM STATMENT

Some questions were been asked in order to derive a meaningful insight on the data. Some of these questions are;

. Who are the top 15 players in FIFA 21?

. Who are the top 5 goalkeepers?

. Who are the top 10 defenders?

. Who is the best central defensive midfielder?

. Who is the overall best player?

. Who are the top 2 strikers?

. Who are the 10 most valueable players in FIFA 21?

. What is the  most populated age group?

. Who are the top 9 footballers with the highest wage?

. Which is the most preferred foot by footballers?

. Top countries that has the highest number of footballer

. Top 5 players with the longest contract duration

. Top 10 players that has the most skill attributes

---

# DATA ANALYSIS AND VISUALIZATION

Analysis was carried out using pivot table, and also pivort chart for building dashboard in Excel.

![1  15 best player](https://user-images.githubusercontent.com/97677904/236262339-8e09fdfa-7340-40b2-8542-b0a959a338aa.jpg)

The picture above depict the best 15 players in FIFA 21. Having L.Messi as the first and T. Courtois as the last 

---

![2  5 goalkepr](https://user-images.githubusercontent.com/97677904/236264314-f07cedd6-8f59-42ae-ad52-395ae308081a.jpg)

Using their goalkeeping attributes to analyse the best 5 goalkeepers, It's seen that M. Neuer is the best goalkeeper followed by M.tr Stegen, Alisson, J. Oblak and Ederson

---

![3  10 defender](https://user-images.githubusercontent.com/97677904/236265759-07bc7598-bee8-4f03-a7fb-db28eac45e9f.jpg)

According to their defending attributes, the above names are the top 10 defenders

---

![4  players with highest wage](https://user-images.githubusercontent.com/97677904/236266779-1ce74c1b-3956-43ce-bc09-410c428753a0.jpg)

The players that get the highest wage are shown above

---

![5  most valuable players](https://user-images.githubusercontent.com/97677904/236267364-5cdc98a9-84dd-48dd-a57b-215c96d56285.jpg)

This shows the 10 most valuable players and it was determined by their market value

---

![6  2 strikers](https://user-images.githubusercontent.com/97677904/236267795-8f894fc2-1e1d-4e8e-9fbc-9a6c6f37fe4b.jpg)

The top 2 strikers are Christiano Ronaldo and Lionel Messi as seen in the above image. This was achieved using their shooting ability

---

![7  country with most players](https://user-images.githubusercontent.com/97677904/236268400-7d863d3e-68fd-45a7-8ca1-f1eb89ab5494.jpg)

The highest number of players originated from England (1705 players) follow by Germany (1195 players), Spain with (1065 players) then France (1003 players), also Argentina (943 players) and Brazil (887) 

---

![8  contract](https://user-images.githubusercontent.com/97677904/236270294-2f3807f3-eccc-4f2e-ba37-0507488e921d.jpg)

H.Sogahata has the longest contract duration (23 years), I.Khune (21 years), I.Akinfeev (20 years), M.Bloomfield and D.Lewington have the same years of contract duration (19 years)

---

![9  skill](https://user-images.githubusercontent.com/97677904/236271997-6d01fd86-c291-479f-a954-c65fcf98135c.jpg)

The above image shows the top players in respect to their skill attributes

---

![14  best  cntra](https://user-images.githubusercontent.com/97677904/236274855-8b6ee54f-39f6-4e04-9c29-7d61459d84f3.jpg)
![10  best central](https://user-images.githubusercontent.com/97677904/236274939-a08eba6d-302e-40ae-99c5-694263542291.jpg)

After thorough analysis, it's concluded that V.van Dijk is the best central defensive midfielder

---

![15  overall](https://user-images.githubusercontent.com/97677904/236276279-748752e1-6914-4a92-9251-c0f6938595b9.jpg)
![11  overall player](https://user-images.githubusercontent.com/97677904/236276320-2d353c1c-304d-426b-9e48-53fbc1ceb380.jpg)

Using the best overall rating the player has achieved in their career helped in determining the overall best player which is Lionel.Messi

---

# ANALYSIS REPORT

![FIFA 21 DASHBOARD 1](https://user-images.githubusercontent.com/97677904/236279093-ca92fa3d-b235-447b-bb87-572fa29633d7.png)

---

CONCLUSION AND RECOMMENDATION

I learnt some concept and procedure while cleaning the data. This really add to my data cleaning knowledge

It is important to know more about a data before starting the cleaning operation process. By doing so, one will get familiar and also be guided on what is expected to be done on the dataset. For instance, with the help of the data dictionary the cleaning was made easier.

Here is the link to the cleaned data:

https://meenah001-my.sharepoint.com/:x:/g/personal/meenah001_meenah001_onmicrosoft_com/Edr-bY8edgJPlUBL4nsa0P0BlIC2OsFGHcZZDrfiM-N_VQ?rtime=XhyWyW9K20g


Link to the dashboard

https://meenah001-my.sharepoint.com/:x:/g/personal/meenah001_meenah001_onmicrosoft_com/EX3Qb7N_NUVDkpRDt67kU1IBe-lDO2GUSvukMCkaCTshuw?e=zJJ2TQ











































































































