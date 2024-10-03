# Movie Dataset Analysis

## Overview

This project provides an analysis of the [Movie Dataset from Kaggle](https://www.kaggle.com/datasets/danielgrijalvas/movies) to explore key aspects of the movie industry such as budget, gross revenue, genre popularity, and more. The dataset includes various information about movies, such as their budget, gross revenue, release year, director, and genre.

The analysis focuses on trends across multiple dimensions and aims to uncover insights about how different genres perform, how movie budgets correlate with gross revenue, and other interesting patterns in the data.

## Dataset Description

The dataset consists of the following columns:

- **name**: Name of the movie
- **rating**: The MPAA rating of the movie (e.g., PG, R)
- **genre**: Genre of the movie (e.g., Action, Comedy)
- **year**: The release year of the movie
- **released**: Release date of the movie (e.g., "January 1, 2000 (USA)")
- **score**: IMDb score of the movie
- **votes**: Number of votes the movie received on IMDb
- **director**: Director of the movie
- **writer**: Writer of the movie
- **star**: Main actor or actress in the movie
- **country**: Country where the movie was produced
- **budget**: Budget of the movie in dollars
- **gross**: Gross revenue of the movie in dollars
- **company**: Production company responsible for the movie
- **runtime**: Movie length in minutes

Additional columns, such as `company-id`, `director-id`, `writer-id`, and `country-id`, are encoded identifiers for categorical features.

## Goals of the Analysis

The project aims to:
1. Analyze the **relationship between movie budgets and gross revenue**, and identify trends.
2. Explore **genre distribution** across years and its impact on budget and revenue.
3. Study **correlations** between important numerical features such as budget, gross, IMDb scores, and votes.
4. Gain insights into the **popularity of different genres** over the last 10 years.
5. Understand how **different companies and directors** perform in terms of budget and revenue.
6. Visualize key relationships and insights using **plots and heatmaps**.

## Key Analysis

### 1. **Budget vs Gross Revenue**
- A scatter plot was created to explore the relationship between movie budgets and gross revenues.
- **Finding**: Higher budgets generally lead to higher gross revenue, but there are many outliers where low-budget films perform extremely well.

### 2. **Genre Popularity Over Time**
- The dataset was grouped by **genre** and **year**, and the count of movies was visualized for the last 10 years.
- **Finding**: Some genres like **Action** and **Drama** have consistently high movie counts, while others like **Western** or **Musical** show significantly fewer movies over the years.

### 3. **Mean Budget by Genre**
- The average budget for each genre was computed to understand which genres tend to have the highest financial backing.
- **Finding**: **Animation** and **Action** tend to have the highest budgets, while **Comedy** and **Horror** have comparatively lower budgets.

### 4. **Correlation Study**
- A correlation matrix was computed to study relationships between numerical features (e.g., budget, gross, votes, score).
- **Finding**: There’s a strong positive correlation between **budget** and **gross**, as well as between **votes** and **gross**. However, IMDb scores have a weaker correlation with budget and gross.

### 5. **Handling Missing Data**
- Missing values in columns such as `rating`, `released`, `votes`, and `country` were identified and handled appropriately during analysis.

### 6. **Year Extraction from Release Date**
- The `released` column, which contains the full date along with the country of release, was processed to extract only the year. This was necessary to group movies by release year for some of the analyses.

### 7. **Visualizing the Last 10 Years**
- The dataset was filtered to focus on the last 10 years of data, and visualizations were created to analyze how genres and budget distributions have evolved in this period.

### 8. **Removing Columns with Zero Values**
- Columns that consisted entirely of zero values were removed from the dataset to clean up the analysis and focus on relevant features.

## Key Visualizations

The following visualizations were created as part of the analysis:

- **Scatter Plot**: Shows the relationship between `budget` and `gross` revenue to explore the financial dynamics of movies.
- **Bar Chart**: Displays the count of movies in each genre over the last 10 years.
- **Heatmap**: Shows the correlation matrix between key numerical features such as budget, gross, votes, and IMDb score.
- **Line Chart**: Visualizes how the number of movies released in each genre has changed over time, especially focusing on recent years.

## Usage Instructions

### 1. **Requirements**
To run the analysis, you need the following Python packages installed:

```bash
pip install pandas matplotlib seaborn numpy jupyter
```

### 2. **Running the Notebook**
To reproduce the analysis:

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/danielgrijalvas/movies) and save it as `movies.csv`.
2. Open `movies_analysis.ipynb` in Jupyter Notebook or JupyterLab.
3. Ensure the dataset is loaded correctly and run each cell in the notebook sequentially to complete the analysis.

### 3. **Customization**
Feel free to modify the analysis or visualizations by adjusting the code in the notebook. You can focus on specific genres, companies, or time periods to suit your research interests.

## Conclusion

This project provides a comprehensive analysis of the movie dataset, focusing on financial performance, genre trends, and correlations between key variables. The insights gained can help understand the dynamics of the movie industry, such as which genres are most popular, how budget impacts revenue, and what correlations exist between movie success metrics.

## Future Work

In future iterations of this analysis, the following areas can be explored:

- Incorporating **machine learning models** to predict movie revenue based on features like genre, budget, and director.
- Adding more granular financial data, such as **international vs. domestic revenue**, to provide deeper insights into global box office trends.
- Analyzing the **impact of star power** by looking at the performance of movies with specific actors or actresses.

