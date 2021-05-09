# Assessment 4: Reproducible Data Analysis Project
# Joel Scrivener ~ u3227529

## About the Project

I am a data analyst with the Chicago Bulls in the NBA, tasked with identifying
the five best starting players that the team can afford. Our player salary 
budget for the coming season is **$118 million**.

The following project utilises data from the most recent season (2018-19) to 
build a model for predicting wins in the NBA, before applying that model to 
value and select individual players. The project includes all stages of this 
process, including:

* Reading and storing the data;
* Exploratory analysis;
* Data modelling and results;
* Player recommendations.

The project has been built using R, with data provided by 
basketball-reference.com and hoopshype.com.

## Required R Packages

The project utilises several non-base packages that may require installation 
prior to use. These are:

* tidyverse
* broom
* janitor
* corrplot
* plotly
* ggrepel
* naniar
* car

## Repository Contents

This repository contains the following the following files/folders:

* **jscrivener_u3227529_a4.Rmd** - The raw R Markdown file used to generate the main
report;
* **jscrivener_u3227529_a4.md** - A markdown file generated from the R Markdown file
so the rendered report can be viewed in Github;
* **jscrivener_u3227529_a4.html** - The main report itself, detailing the entire
process of the project;
* **README.md** - Outlining the repository contents and background information required  to understand the project;
* **10157A4-Jscrivener-u3227529.Rproj** - An Rstudio project file used to 
organise the project during development;
* **background.css** - A css file setting out the Chicago Bulls logo as a background
watermark in the html report;
* **/data** - A data folder, containing /raw (raw csv files used in the project) and
* **/processed** (processed files following tidying);
* **/figs** - A figures folder, containing figures rendered from the project;
* **/images** - An images folder, containing the Chicago Bulls logo referenced in 
the background.css file.

## Variable Descriptions

The following are descriptions of the variables contained within each of the 
data sets used in the project.

### 2018-19_nba_player-salaries.csv

* **player_id** : unique player identification number
* **player_name** : player name
* **salary** : year salary in $USD

### 2018-19_nba_player_statistics.csv


* **player_name** : Player Name
* **Pos** :  (PG = point guard, SG = shooting guard, SF = small forward, PF = power 
forward, C = center) 
* **Age** : Age of Player at the start of February 1st of that season.
* **Tm** : Team
* **G** : Games
* **GS** : Games Started
* **MP** : Minutes Played
* **FG** : Field Goals
* **FGA** : Field Goal Attempts
* **FG%** : Field Goal Percentage
* **3P** : 3-Point Field Goals
* **3PA** : 3-Point Field Goal Attempts
* **3P%** : FG% on 3-Pt FGAs
* **2P** : 2-Point Field Goals
* **2PA** : 2-point Field Goal Attempts
* **2P%** : FG% on 2-Pt FGAs
* **eFG%** : Effective Field Goal Percentage
* **FT** : Free Throws
* **FTA** : Free Throw Attempts
* **FT%** : Free Throw Percentage
* **ORB** : Offensive Rebounds
* **DRB** : Defensive Rebounds
* **TRB** : Total Rebounds
* **AST** : Assists
* **STL** : Steals
* **BLK** : Blocks
* **TOV** : Turnovers
* **PF** : Personal Fouls
* **PTS** : Points

### 2018-19_nba_team_statistics_1.csv

* **Rk** : Rank
* **Age** : Mean Age of Player at the start of February 1st of that season.
* **W** : Wins
* **L** : Losses
* **PW** : Pythagorean wins, i.e., expected wins based on points scored and allowed
* **PL** : Pythagorean losses, i.e., expected losses based on points scored and 
allowed
* **MOV** : Margin of Victory
* **SOS** : Strength of Schedule; a rating of strength of schedule. The rating is 
denominated in points above/below average, where zero is average.
* **SRS** : Simple Rating System; a team rating that takes into account average 
point differential and strength of schedule. The rating is denominated in points
above/below average, where zero is average.
* **ORtg** : Offensive Rating; An estimate of points produced (players) or scored 
(teams) per 100 possessions
* **DRtg** : Defensive Rating; An estimate of points allowed per 100 possessions
* **NRtg** : Net Rating; an estimate of point differential per 100 possessions.
* **Pace** : Pace Factor: An estimate of possessions per 48 minutes
* **FTr** : Free Throw Attempt Rate; Number of FT Attempts Per FG Attempt
* **3PAr** : 3-Point Attempt Rate; Percentage of FG Attempts from 3-Point Range
* **TS%** : True Shooting Percentage; A measure of shooting efficiency that takes 
into account 2-point field goals, 3-point field goals, and free throws.
* **eFG%** : Effective Field Goal Percentage; This statistic adjusts for the fact 
that a 3-point field goal is worth one more point than a 2-point field goal.
* **TOV%** : Turnover Percentage; An estimate of turnovers committed per 100 plays.
* **ORB%** : Offensive Rebound Percentage; An estimate of the percentage of 
available offensive rebounds a player grabbed while he was on the floor.
* **FT/FGA** : Free Throws Per Field Goal Attempt
* **DRB%** : Defensive Rebound Percentage

### 2018-19_nba_team-statistics_2.csv


* **Rk** : Ranking
* **Team** : Team name
* **G** : Games
* **MP** : Minutes Played
* **FG** : Field Goals
* **FGA** : Field Goal Attempts
* **FG%** : Field Goal Percentage
* **3P** : 3-Point Field Goals
* **3PA** : 3-Point Field Goal Attempts
* **3P%** : FG% on 3-Pt FGAs
* **2P** : 2-Point Field Goals
* **2PA** : 2-point Field Goal Attempts
* **2P%** : FG% on 2-Pt FGAs
* **FT** : Free Throws
* **FTA** : Free Throw Attempts
* **FT%** : Free Throw Percentage
* **ORB** : Offensive Rebounds
* **DRB** : Defensive Rebounds
* **TRB** : Total Rebounds
* **AST** : Assists
* **STL** : Steals
* **BLK** : Blocks
* **TOV** : Turnovers
* **PF** : Personal Fouls
* **PTS** : Points

## Acknowledgements

Thanks to Dr Jocelyn Mara for a cracking semester, and for providing the skills
required to actually complete this mammoth project. 
