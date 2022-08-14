# Application

## Challenge: Crypto Arbitrage

![Decorative image.](Images/3-5-bitcoin-718303837.png)

### Background

In this Challenge, you'll take on the role of an analyst at a high-tech investment firm. The vice president (VP) of your department is considering arbitrage opportunities in Bitcoin and other cryptocurrencies. As Bitcoin trades on markets across the globe, can you capitalize on simultaneous price dislocations in those markets by using the powers of Pandas?

For this assignment, you’ll sort through historical trade data for Bitcoin on two exchanges: Bitstamp and Coinbase. Your task is to apply the three phases of financial analysis to determine if any arbitrage opportunities exist for Bitcoin.

### What You're Creating

You’ll create a Jupyter notebook that contains the code for your data collection, preparation, and analysis, including any visualizations. Within the same notebook file, you should use comments and text to document your analysis, including the answers to the questions in the Challenge instructions. Make this report clear and concise. Add appropriate comments to the code, and include any necessary labels for the visualizations. Remember that you’ll present this report to your VP!

To accomplish these tasks, you’ll perform the following phases of financial analysis:

1. Collect CSV data in a Jupyter notebook file.
2. Prepare the datasets for analysis by cleaning missing and erroneous data.
3. Analyze the data at a high level through summary statistics and visualizations, and use this information to select areas for deeper analysis. Specifically, you’ll select time periods in which to identify arbitrage opportunities.

### Files

Download the following files to help you get started:

[Module 3 Challenge files](https://fintech-blended-curriculum.s3.amazonaws.com/Module+3/Starter_Code.zip)

### Instructions

This Challenge consists of the following steps:

1. Create your GitHub repository.
2. Collect the data.
3. Prepare the data.
4. Analyze the data.
5. Create your analysis report.

#### Create Your GitHub Repository

In this section, you’ll create the GitHub repository for this Challenge. To initialize the repository, use the `Resources` folder and the `crypto_arbitrage.ipynb` notebook provided in the `Starter_Code` folder. Then complete the following steps:

1. Create a `README.md` file for the Challenge.

2. Create a `.gitignore` file to exclude the files that you don’t want to include in your repository.

3. Upload your Jupyter notebook to the repository.

> **Important** Make sure to commit and push your changes as you progress through the Challenge.

#### Collect the Data

To collect the data that you’ll need, complete the following steps:

1. Using the Pandas `read_csv` function and the `Path` module, import the data from `bitstamp.csv` file, and create a DataFrame called `bitstamp`. Set the DatetimeIndex as the Timestamp column, and be sure to parse and format the dates.

2. Use the `head` (and/or the `tail`) function to confirm that Pandas properly imported the data.

3. Repeat Steps 1 and 2 for `coinbase.csv` file.

#### Prepare the Data

To prepare and clean your data for analysis, complete the following steps:

1. For the bitstamp DataFrame, replace or drop all `NaN`, or missing, values in the DataFrame.

2. Use the `str.replace` function to remove the dollar signs ($) from the values in the Close column.

3. Convert the data type of the Close column to a `float`.

4. Review the data for duplicated values, and drop them if necessary.

5. Repeat Steps 1–4 for the coinbase DataFrame.

#### Analyze the Data

Your analysis consists of the following tasks:

* Choose the columns of data on which to focus your analysis.

* Get the summary statistics and plot the data.

* Focus your analysis on specific dates.

* Calculate the arbitrage profits.

##### Choose the Columns of Data

Select the data you want to analyze. Use `loc` or `iloc` to select the following columns of data for both the bitstamp and coinbase DataFrames:

* Timestamp (index)

* Close

##### Get the Summary Statistics and Plot the Data

Sort through the time series data associated with the bitstamp and coinbase DataFrames to identify potential arbitrage opportunities. To do so, complete the following steps:

1. Generate the summary statistics for each DataFrame by using the `describe` function.

2. For each DataFrame, create a line plot for the full period of time in the dataset. Be sure to tailor the figure size, title, and color to each visualization.

3. In one plot, overlay the visualizations that you created in Step 2 for bitstamp and coinbase. Be sure to adjust the legend and title for this new visualization.

4. Using the `loc` and `plot` functions, plot the price action of the assets on each exchange for different dates and times. Your goal is to evaluate how the spread between the two exchanges changed across the time period that the datasets define. Did the degree of spread change as time progressed?

##### Focus Your Analysis on Specific Dates

Focus your analysis on specific dates by completing the following steps:

1. Select three dates to evaluate for arbitrage profitability. Choose one date that’s early in the dataset, one from the middle of the dataset, and one from the last year of the time period.

2. For each of the three dates, generate the summary statistics and then create a box plot. This big-picture view is meant to help you gain a better understanding of the data before you perform your arbitrage calculations. As you compare the data, what conclusions can you draw?

##### Calculate the Arbitrage Profits

Calculate the potential profits for each date that you selected in the previous section. Your goal is to determine whether arbitrage opportunities still exist in the Bitcoin market. Complete the following steps:

1. For each of the three dates, measure the arbitrage spread between the two exchanges by subtracting the lower-priced exchange from the higher-priced one. Then use a conditional statement to generate the summary statistics for each arbitrage_spread DataFrame, where the spread is greater than zero.

2. For each of the three dates, calculate the spread returns. To do so, divide the instances that have a positive arbitrage spread (that is, a spread greater than zero) by the price of Bitcoin from the exchange you’re buying on (that is, the lower-priced exchange). Review the resulting DataFrame.

3. For each of the three dates, narrow down your trading opportunities even further. To do so, determine the number of times your trades with positive returns exceed the 1% minimum threshold that you need to cover your costs.

4. Generate the summary statistics of your spread returns that are greater than 1%. How do the average returns compare among the three dates?

5. For each of the three dates, calculate the potential profit, in dollars, per trade. To do so, multiply the spread returns that were greater than 1% by the cost of what was purchased. Make sure to drop any missing values from the resulting DataFrame.

6. Generate the summary statistics, and plot the results for each of the three DataFrames.

7. Calculate the potential arbitrage profits that you can make on each day. To do so, sum the elements in the profit_per_trade DataFrame.

8. Using the `cumsum` function, plot the cumulative sum of each of the three DataFrames. Can you identify any patterns or trends in the profits across the three time periods?

#### Create Your Analysis Report

Write your final report by using text or comments within your Jupyter notebook file. This report should summarize your analysis and include the following:

* Assumptions or discoveries that you made during the analysis

* Summary tables and calculations

* Visualizations

> **Important** Make sure to commit and push your final changes to GitHub. Also, before submitting your project, update the `README.md` file to include general information about your analysis. Include information about the datasets—their names and beginning and end dates—and the libraries you used in the analysis.

### Requirements

#### Create Your GitHub Repository (10 points)

##### To receive all points, you must:

* Create a `README.md` file for the Challenge. (3 points)
* Create a `.gitignore` file to exclude the files that you don’t want to include in your repository. (3 points)
* Upload your Jupyter notebook to the repository. (4 points)

#### Collect the Data (10 points)

##### To receive all points, your code must:

* Using the Pandas `read_csv` function, import the data from `bitstamp.csv` and create a DataFrame called bitstamp. Set the index as the Timestamp column, and be sure to parse and format the dates. (3 points)
* Use the `head` (and/or the `tail`) function to confirm that Pandas properly imported the data. (3 points)
* Repeat Steps 1 and 2 for `coinbase.csv`. (4 points)

#### Prepare the Data (10 points)

##### To receive all points, your code must:

* For the bitstamp DataFrame, replace or drop all `NaN`, or missing, values in the DataFrame. (2 points)
* Use the `replace` function to remove the dollar signs ($) from the values in the Close column. (2 points)
* Convert the data type of the Close column to a `float`. (2 points)
* Review the data for duplicated values, and drop them if necessary. (2 points)
* Repeat the four preceding steps for the coinbase DataFrame. (2 points)

#### Analyze the Data (20 points)

##### To receive all points, your code must:

* Get the summary statistics and plot the data. (5 points)
* Focus your analysis on specific dates. (5 points)
* Calculate the arbitrage profits. (10 points)

#### Create Your Analysis Report (20 points)

##### To receive all points, your report must include:

* Assumptions or discoveries that you made during the analysis (10 points)
* Summary tables and calculations (5 points)
* Visualizations (5 points)

#### Coding Conventions and Formatting (10 points)

##### To receive all points, your code must:

* Place imports at the beginning of the file, just after any module comments and docstrings and before module globals and constants. (3 points)
* Name functions and variables with lowercase characters and with words separated by underscores. (2 points)
* Follow Don't Repeat Yourself (DRY) principles by creating maintainable and reusable code. (3 points)
* Use concise logic and creative engineering where possible. (2 points)

#### Deployment and Submission (10 points)

##### To receive all points, you must:

* Submit a link to a GitHub repository that’s cloned to your local machine and contains your files. (4 points)
* Use the command line to add your files the repository. (3 points)
* Include appropriate commit messages in your files. (3 points)

#### Code Comments (10 points)

##### To receive all points, your code must:

* Be well commented with concise, relevant notes that other developers can understand. (10 points)

### Submission

To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

> **Note** You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next Module.

Comments are disabled for graded submissions in BootCamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Manager. If you would like to resubmit your work for an improved grade, you can use the Resubmit Assignment button to upload new links.  You may resubmit up to three times for a total of four submissions.

## Career Connection

Welcome to another Career Connection! This week, you built on your Python skills by learning Pandas, one of the most popular Python libraries for data analysis. Now, you'll dive more deeply into how you might use Pandas in the workplace&mdash;and into some career pathways in the world of fintech.

Here’s the Career Connection agenda for today:

* Pandas in the Workplace

* Finding Your Career Fit: Exploring Careers in Fintech

* Interview Prep

* Next Steps

### Pandas in the Workplace

If you land a position that involves data analytics, you’ll almost certainly use Pandas on the job. (Don’t worry. By the end of this course, you’ll be extremely familiar with Pandas.) Pandas is one of the most popular Python libraries. It’s known for turning what could be lots of work into a bit of work. In fact, some even attribute the rapid growth of Python to the Pandas library ([Why is Python Growing So Quickly?](https://stackoverflow.blog/2017/09/14/python-growing-quickly/)).

So in fintech, what do we use Pandas for? As you’ve already learned, Pandas is a powerful data analysis tool. In fintech, people use it for machine learning, data analysis, forecasting projects, and modeling. Here are a few examples of how companies are using Pandas:

* Zopa uses Pandas to enhance its peer-to-peer lending services.

* Chime uses Pandas to build the machine learning capabilities of its platform.

* Morgan Stanley uses Pandas to build and maintain its global data assets.

Your new knowledge of Pandas is setting you up for success in your next role. It’s an essential skill for most fintech professionals.

### Finding Your Career Fit: Exploring Careers in Fintech

![alt = "Research"](Images/FinTech-Career-Connection-Research.png)

Recall that finding your career fit consists of six phases: Research, Network, Application Materials, Interviews, Job Offers, and On the Job. Today, you’ll continue with the Research phase.

Something that we find exciting about fintech is the number of career pathways. For example, the completion of this course might lead you to portfolio management, blockchain development, or stock trading. Today, we’ll discuss some of the options.

We recommend reading through the following list of common fintech job titles and researching any that interest you:

**Note:** You might not be qualified for all these positions after the course, but we want to show you what the fintech world has to offer.

* **App Developer:** Develops financial technology apps.

* **Blockchain Developer:** Develops blockchain technologies.

* **Business Development Manager:** Helps fintech companies find ways to generate income.

* **Business Intelligence Analyst:** Creates and analyzes business intelligence needs.

* **Compliance Expert:** Helps ensure that operations comply with law and regulations.

* **Cybersecurity Analyst:** Protects an organization from cyber threats.

* **Data Analyst:** Collects, cleans, and interprets data.

* **Data Scientist:** Develops tools that process and analyze data.

* **Financial Analyst:** Analyzes financial data for internal or external clients.

* **Financial Applications Specialist:** Maintains the optimal performance of applications.

* **Financial Services Strategist:** Helps clients manage financial assets.

* **Product Manager:** Supervises the progress of product development.

* **Quantitative Developer:** Develops financial modeling solutions.

* **Quantitative Trader:** Uses models to identify trading opportunities.

* **Risk & Control Manager:** Establishes policies and procedures that address risks.

Do you have a different job title in mind? Terrific! Fintech is a place for innovation. New job titles are common in the field (for example, blockchain developer is a relatively new title). And, space exists for you to create your own fit.

Finally, we recommend exploring a superb resource that we’ve created for you: the [Career Pathway: FinTech](https://careernetwork.2u.com/career-pathways/fintech/) page in the Career Engagement Network. This resource includes information about fintech certifications, in-demand skills, market trends, and job descriptions.


> **Interview Prep**
>
> Read each of the following questions, enter your answer in a notebook or text file, and then compare your answer to the provided one:
>
> **Note:** The lessons didn’t explicitly cover all the questions. But, the skills and concepts that you learned (plus your research skills) should have prepared you to answer them.
>
> 1. What’s Pandas?
> Answer: Pandas is an open-source library that offers easy-to-use data analysis tools for Python.
>
> 2.  What are the two key data structures in Pandas?
> Answer: The two key data structures in Pandas are the DataFrame and the Series.
>
> 3. What’s a Pandas Series?
> Answer: A Pandas Series is a data container for a sequence of data. It functions like a spreadsheet column and can hold data of any type.
>
> 4. What’s a Pandas DataFrame?
> Answer: A Pandas DataFrame is the equivalent of two or more Series. More importantly, DataFrames allow us to work with rows and columns, or tabular data.
>
> 5. What two Pandas functions do we use to select areas of interest from a larger DataFrame?
> Answer: The two Pandas functions that we use to select areas of interest from a larger DataFrame are `iloc` and `loc`.
>
> 6. How does the syntax of `iloc` differ from that of `loc` for accessing data?
> Answer: The `iloc` function uses the index positions of rows and columns to access data. The `loc` function uses the labels associated with the rows and columns.

### Next Steps

* Consider adding Pandas to the technical skills section of your application materials.

* Further research fintech job titles that interest you.
