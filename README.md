# End-to-End Tidy Data Exploratory Analysis on NBA Data

I cleaned and analyzed NBA rookies' data from 1980 to 2016. Data was collected from Kaggle.

## Table of Contents

1. [Metholody and Purpose](#methodology-and-purpose)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Repo Structure](#repo-structuretier-40-protocol)
5. [Findings](#findings)
6. [Contributing](#contributing)
7. [Liscence](#liscence)

## Methodology and Purpose
I downloaded a freely available dataset from Kaggle regarding NBA rookie data. I cleaned the file by dropping rows with empty values, converting the column headers to lower case, replacing column names with spaces with underscores, and dropping duplicate entries. My intention was to analyze the clean data by plotting graphs to see trends in how rookie metrics have shifted over the years and common and unique statistics among rookies.
## Installation

Go to [Kaggle](https://www.kaggle.com/datasets/thedevastator/nba-rookies-performance-statistics-and-minutes-p) to download the data set.

```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

## Usage
```python
#creates a scatterplot of average points vs. minutes played for a whole season
sns.scatterplot(data = df, y = 'pts', x = 'min', alpha = 0.4)
```

```python
#creates a graph of average 3-point shot attempts in a whole season vs. year drafted 
plt.plot(df['year_drafted'], df['3pa'])
```

## Repo Structure([TIER 4.0 Protocol](https://www.projecttier.org/tier-protocol/protocol-4-0/))
```text
Project/
├── Read_Me_file          
├── The_Report            
├── Data/
│   ├── InputData/
│   │   ├── Input Data Files
│   │   └── Metadata/
│   │       ├── Data_Sources_Guide
│   │       └── Codebooks
│   ├── AnalysisData/
│   │   ├── Analysis Data Files
│   │   └── The_Data_Appendix
│   └── IntermediateData/
|
├── Scripts/
│   ├── ProcessingScripts/   
│   ├── DataAppendixScripts/  
│   ├── AnalysisScripts/
│   └── The_Master_Script
|
└── Output/
    ├── DataAppendixOutput/    
    └── Results/
```

## Findings
Through my graphs, I realized that frmo 1980 to 2016, there has been mostly and upward trend in 3-point shooting. However, watching the NBA, this doesn't suprise me because in the 2010's jumpshooting became increasing more relevant as it was revolutionzed by Stephen Curry and Klay Thompson. Some peak years saw over an average of 6-point attempts per game by rookies!
  
I also found out that that the bulk of rookies score around 2-6 points per game in their rookie season. However, there are some outliers with some rookies scoring above 20 points per game(like Joel Embiid) and in some cases even above 25! For the lower points, this isn't surpising as rookies may not be entrusted with much playing time, especially in tighter games and later on in the season where every game counts. But, another thing to consider is that maybe points(among other statistics) are more inflated due to stat padding in garbage minutes. This could lead to further analysis on how valuable those points are(i.e. what time did they come in: garbage, clutch, regular), as some rookies were part of their starting fives in their rookie seasons like Tim Duncan.
  
Finally, the most suprising element I found was that the more minutes a rookie played, the more points they were likely to score. This indicates that given enough playing time, rookies can make a significant impact. Their stats won't be stagnant. This data can help coaches to entrust them to more playing time. However, this doesn't take into account other elements occuring in those minutes such as turnovers, or defensive liability issues. Another thing to be said by this find is that those who were given more minutes were already good enough to be entrusted to those minutes. This data could be much more insightful had I included every game for each rookie in their season. This way, we could see the impact of minutes on offensive production not just for each player, but each game for a player in whichever minute range. This allows us to see what happens for those players if they are given more or less minutes.
  
## Contributing

You are more than welcome to add graphs and find other insights in this project. Let me know of your findings! Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. 

## Liscence
[MIT](https://choosealicense.com/licenses/mit/)


