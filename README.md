# Loan Data Exploration
## Prosper Loan Data Exploration 
**Overview**
* This project focuses on using Python's data visualization tools to systemicaly explore a Prosper loan dataset for its properties and relationships between variables. The end goal of this project is to create a presentation that communicates these findings to others. The final slide deck can be found in this repo, titled 'presentation_slide_deck.ipynb.'

**About Prosper**
* [Prosper](https://www.prosper.com/) is a San Francisco-based, peer-to-peer lender that provides personal loans to borrowers with fair or good credit. One of its subsidiaries, Prosper Funding LLC, operates on a website where individuals can either request to borrow money or invest in personal loans. To qualify applicants, Prosper rates borrowers using a risk-rating system that factors in hundreds of data points, including credit history. Investors use these ratings to decide whether to fund the requested loan. Each loan comes with a three to five year term. Since its founding in 2005, Prosper has originated more than $16 billion in loans and serviced over 980,000 people. 

## Dataset
The dataset contains information for over 100,000 prosper loans. Each row contains information about a specific loan that was funded through the Prosper marketplace. The DataSet can be found on the [Prosper webpage](https://www.prosper.com/tools/?referral=Spider5) and downloaded [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv). Prosper loan variable definitions can be found [on this page](https://www.prosper.com/Downloads/Services/Documentation/ProsperDataExport_Details.html) for additional context.

## Software
* Python and libraries:
  * Matplotlib
  * NumPy
  * pandas
  * Seaborn
* Jupyter Notebooks

## Summary of Findings
**Distribution of Loans by Year, Month, and Day of Month**

> There is an upward trend with number of loans increasing each year. January has the highest amount of loans listed with April being the lowest and not much variation based on day of the month.

**Distribution of Borrower APR**

> The distribution of APR looks multimodal with a small peaks centered at 0.1 and 0.3 and a sharp peak between 0.35 and 0.36. There are very few loans with an APR greater than 0.4.

**Borrower APR vs. Ratings**

> As prosper ratings increase borrower APR decreases. Borrower's with the highest Prosper ratings have the lowest APR indicating a strong influence on borrower APR.

**Borrower APR vs. Occupation**

> Borrower APR varies with occupation. Students in technical school have the lowert average APR and college juniors have the highest average rating.

**Borrower APR vs Loan Amounts**

> Borrower APR has a large range based on original loan amount. This range decreases as the original loan amount decreases indicating an overall negative correlation between borrow APR and original loan amount.

**The Effects of Ratings on APR and Original Loan Amount**

> Borrower APR decreases as ratings increase. High ratings also lead to an increase in original loan amount. In ratings above B, we start to see an increase in APR associated with larger loan amounts. One possible explanation for this observation would be that the borrowers with A and AA ratings tend to borrow larger amounts and an increased APR prevents them from taking out larger loans while maximizing profits. Conversely, APR decreases with increasing loan amounts for borrowers with lower ratings of C, D, E, and HR. Since people with lower ratings typically loan smaller amounts, the decrease in APR with larger loans encourges those with lower ratings to borrow more.

**Borrower APR by Prosper Rating and Term**

> For borrowers with ratings HR through C, APR decreases as term increases. For those with ratings greater than B, there is an increasing APR associated with longer terms.

**Prosper Ratings by Monthly Income, Loan Amount, and Term**

> For stated monthly income, there doesn't seem to be an interaction between term and rating. The pattern is similar among different ratings. Here we do see a relationship between term and rating based on loan amount. With increasing ratings, we see an increase in all three terms. We also see that the amplitude for original loan amounts between terms increases with higher ratings.

## Credits
* https://matplotlib.org/3.1.0/gallery/color/named_colors.html
* https://matplotlib.org/tutorials/intermediate/legend_guide.html
* https://medium.com/@morganjonesartist/color-guide-to-seaborn-palettes-da849406d44f
* https://www.prosper.com/Downloads/Services/Documentation/ProsperDataExport_Details.html
* https://www.prosper.com/tools/?referral=Spider5
* https://seaborn.pydata.org/generated/seaborn.FacetGrid.html
* https://stackoverflow.com/questions/51579215/remove-seaborn-lineplot-legend-title
* https://stackoverflow.com/questions/31594549/how-do-i-change-the-figure-size-for-a-seaborn-plot
* https://stackoverflow.com/questions/31517194/how-to-hide-one-specific-cell-input-or-output-in-ipython-notebook
* https://www.udacity.com/course/data-analyst-nanodegree--nd002
