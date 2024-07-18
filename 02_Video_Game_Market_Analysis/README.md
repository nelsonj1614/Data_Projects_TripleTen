# Video Game Market Analysis

**Project:** Discover patterns and insights in historical video game sales data for an upcoming advertising campaign. 

<div align="center">
    <img alt="gaming" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/9660385abc0252026fe3eb86bd539e1b6cdf010f/02_Video_Game_Market_Analysis/Photos/pexels-kowalievska-1174746.jpg">
</div>

<br>

## Business Problem
The online store, Ice, sells video games all over the world. User and expert reviews, genres, platforms (e.g. Xbox or PlayStation), and historical data on game sales are available from open sources. Ice wants to identify patterns that determine whether a game succeeds or not. This will allow them to spot potential big winners and plan advertising campaigns. The campaign is planned for 2017. The data provided runs up to 2016. 

The dataset contains the abbreviation ESRB. The Entertainment Software Rating Board evaluates a game's content and assigns an age rating such as Teen or Mature.

**Data:** Data consists of 1 CSV file. Features include:


## Solution Strategy

**Step 1: Data Description and Cleaning**

**Step 2: Feature Engineering**

**Step 3: Data Analysis**

**Step 4: Create Regional User Profiles**

**Step 5: Hypothesis Testing**

## Key Data Insights

#### Insight 1: Games Released by Year

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/f4a695a6a107a6614c3d1fab166e42dabb97b044/02_Video_Game_Market_Analysis/Photos/vg1.png">
</div>

There is an increase in games in the mid 1990s and then a larger increase in the early 2000s, climaxing around 2008/2009.

#### Insight 2: Total Sales by Year by Platform

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/f4a695a6a107a6614c3d1fab166e42dabb97b044/02_Video_Game_Market_Analysis/Photos/vg2.png">
</div>

The highest distribution falls from around the year 2005 to 2011. Platforms tend to have a 6 - 10 year lifespan. The distribution of sales over time generally follows a normal distribution. Now that I know the trends consoles tend to follow, I can set the time frame for limiting my dataset. Given the above analysis, I will limit my analysis to video game releases from the past 3 years. Judging from the lifespans of the platforms, data within this range includes games and consoles that are still popularly sold.

#### Insight 3: Top 3 Platforms (Sales by Year)

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/f4a695a6a107a6614c3d1fab166e42dabb97b044/02_Video_Game_Market_Analysis/Photos/vg3.png">
</div>

While the 3DS did not follow a normal distribution, the PS4 and Xbox One seem to be following the curve. Given that data for 2016 may not be complete (assuming that the analysis is done in 2016 in preparation for 2017), actual sales for PS4 and Xbox One may be higher than observed in the dataset. Successful older consoles tended to have a lifespan from 6 - 10 years, therefore these consoles may not have hit their climax yet.

#### Insight 4: Game Genre Sales

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/f4a695a6a107a6614c3d1fab166e42dabb97b044/02_Video_Game_Market_Analysis/Photos/vg4.png">
</div>

Action games are the genre most often produced. The Role-Playing genre, the 2nd highest, is only about 1/3 of the size of the Action genre. Puzzle games had the smallest count at less than 100 games produced.

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/f4a695a6a107a6614c3d1fab166e42dabb97b044/02_Video_Game_Market_Analysis/Photos/vg5.png">
</div>

Although Action games lead both the count and sales lists, the margin is greatly reduced and the order has changed. Shooter games, 5th highest in the count chart, make up over 150 in sales. Sports also follows a similar pattern, with fewer games produced but significantly higher sales. Genres near the end of the list such as puzzle and strategy, however, remain in the same position on both charts.

#### Insight 5: Sales Distributions by Genre

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/f4a695a6a107a6614c3d1fab166e42dabb97b044/02_Video_Game_Market_Analysis/Photos/vg6.png">
</div>

Distribution of sales by genre follows a similar distribution with a positive skew given the great number of outliers. This reflects findings that were suggested with the box plots we plotted above.

## Regional User Profiles

#### Region 1: North America

- **Top 5 Platforms:**

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp1.1.png">
</div>

- **Top 5 Genres:**

<div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp1.2.png">
</div>
  
- **Ratings:**

  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp1.3.png">
</div>

- **Summary:**

The top 5 platforms in North America are:
- PS4
- Xbox One
- Xbox 360
- 3DS
- PS3

The top 5 genres in North America are:
- Shooter
- Action 
- Sports 
- Role-Playing 
- Misc

**Rating:** Comparing sales by rating in North America and overall shows a similar distribution. Mature games are most profitable overall and the same is true in North America. Therefore, game ratings do not significantly affect sales in North America.

#### Region 2: Europe

- **Top 5 Platforms:**
  
  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp2.1.png">
</div>

- **Top 5 Genres:** 

  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp2.2.png">
</div>

- **Ratings:**

  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp2.3.png">
</div>

- **Summary:**

The top 5 platforms in Europe are:
- PS4
- Xbox One
- PS3
- PC
- 3DS

The top 5 genres in Europe are:
- Action 
- Shooter 
- Sports 
- Role-Playing 
- Racing

**Ratings:** When compared to total sales by rating, we get the same distribution. Therefore, game ratings do not significantly alter game sales in Europe.

#### Region 3: Japan

- **Top 5 Platforms:**
  
  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp3.1.png">
</div>

- **Top 5 Genres:** 

  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp3.2.png">
</div>

- **Ratings:**

  <div align="center">
    <img alt="vg" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/457d299ed67b62a097d961b6ad02070d84e57675/02_Video_Game_Market_Analysis/Photos/rp3.3.png">
</div>

- **Summary:**

The top 5 platforms in Japan are:
- 3DS 
- PS4 
- PSV 
- PS3 
- WiiU

The top 5 genres in Japan are:
- Role-Playing
- Action 
- Fighting
- Misc 
- Shooter

**Ratings:** The fact that games rated Mature brought in the 2nd least sales in Japan suggests that higher game ratings affect sales.
