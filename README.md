# Sampling Bias and Mean Reversion in Football Analytics

This project delves into the concepts of sampling bias and mean reversion within the realm of football analytics. By understanding the patterns and nature of the data, it aims to uncover how these statistical phenomena influence data interpretation and decision-making. The project focuses on identifying how to treat data—whether good or bad—while creating a roadmap for analyzing trends, finding the next direction, and improving predictive models in football analytics.

## Table of Contents
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [Contributing](#contributing)
- [License](#license)

## Introduction
Sampling bias and mean reversion are critical concepts in statistics that can significantly impact the analysis of football data. This project investigates these concepts and demonstrates their implications through real-world football datasets.

## Objectives
- Understand the effects of sampling bias in football analytics.
- Analyze mean reversion trends in player and team performance.
- Develop tools to mitigate bias and improve predictive models.

## Methodology
1. Data collection from football datasets.
2. Identification and analysis of sampling bias.
3. Examination of mean reversion patterns.
4. Visualization and reporting of findings.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## How to Run
1. Clone the repository:
    ```bash
    git clone https://github.com/DhawaDG/Sampling_Bias_and_Mean_Reversion_in_Football_Analytics
    ```
2. Navigate to the project directory:
    ```bash
    cd football-analytics
    ```
3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## Challenge
## Challenge

1. **Error and Solution: Invalid Line Style in `plt.axhline`**  
   While working on `05_Population_mean_Vs_Sample_mean.ipynb`, an error occurred:  
   `ValueError: '**' is not a valid value for ls; supported values are '-', '--', '-.', ':', 'None', ' ', '', 'solid', 'dashed', 'dashdot', 'dotted'`.  
   This was caused by an incorrect value for the `linestyle` parameter in `plt.axhline`. The issue was resolved by replacing the invalid value with a valid one, such as `'--'`.  
   **Corrected Code:**  
   ```python
   plt.axhline(y=mean, color='green', linestyle='--', label=f'Sample Mean: {mean:.2f}')

2. **Text Annotation for Bar Values**

    In 06_Selection_Bias(Detecting Fake Patterns).ipynb, adding text annotations to label bar values was a challenge. The solution involved using plt.text within a loop to place the labels above each bar.
   
    **Example Code:**
    ```python
    for i, val in enumerate(averages):
    plt.text(i, val + 0.1, f'{val:.2f}', ha='center', fontsize=12)

 3. **Understanding and Implementing pivot()**
   In 07_Regression_to_mean.ipynb, creating a pivot table to compare player performance across two seasons was moderately challenging. The pivot() function was used to restructure the data, and the top 5 players were selected for visualization.

**Key Code Snippet:**
    ```python
    pivot_df = df.pivot(index='Player', columns='Season', values='G+A').dropna()
    pivot_df.columns = ['G+A_2022_23', 'G+A_2023_24']
    top_5 = pivot_df.sort_values('G+A_2022_23', ascending=False).head(5)

5. Other Challenges

- Simulating realistic player performance data for two seasons and ensuring the data aligns with statistical principles.
- Visualizing the regression to the mean effectively using bar plots and ensuring the plot is clear and informative.
- Managing large datasets and ensuring the code is efficient and scalable.

