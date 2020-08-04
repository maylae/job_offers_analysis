# job_offers_analysis
1. Installations
Here are the prerequisites you need to run the notebook
- Python version 3.8.3
- Libraries
	- pandas
	- numpy
	- plotly
	- seaborn
	- datetime
	- re

2. Project Motivation
Data Analyst/Scientist jobs become more and more attractive. Therefore, it seems interesting to take a look at job offers in this area and find the data science hotspots in the US and where job applicants can expect the highest salaries. This analysis is part of an online course for Data Scientists.

3. File Descriptions
The Jupyter notebook Data Analysis for Data Analyst Job Offers on Glassdoor.ipynb contains all data preparations for this project. You find the input dataset in the file DataAnalyst.csv.

4. Method
In this project, I examined characteristics of Data Analyst job offers on Glassdoor.
Following the CRISP-DM process, I followed the phases depicted below. The steps taken in each phase are explained in the following.
	- Business Understanding
		When looking at job offers for Data Analyst jobs, I put together several questions that might be interesting for aspiring data analysts:
		1. Do bigger/older companies offer higher salaries?
		2. Which sectors are looking for data analysts? And which ones pay best?
		3. Where are the most data analyst jobs offered? 
	- Data Understanding
		The basis for my analysis is a dataset that was provided on Kaggle (see Acknowledgements) which contains ca. 2500 data analyst job offers scraped from Glassdoor in July 2020. It contains 16 columns, of which three are numerical and 13 categorical. Next to a job description, the information on the job offers contains the company's name, location, headquarter location, revenue, industry, sector, competitors, size and age as well as a salary estimate provided by Glassdoor.
	- Data Preparation
		At first, some columns that were not needed for analysis were dropped.
		Missing values marked by -1 in the dataset were kept since no dummy variables needed to be created and the rows with missing data in one columns could still be used for other questions. Only one row where the salary estimate was missing was dropped to avoid errors in further data preparation and because it was only one row.
	- Modeling
		To answer the questions, basic descriptive statistics were used.
		1. Do bigger/older companies offer higher salaries?
			This question was answered by dropping missing values for the Size and Company Age column and calculating the mean. 
			No linear relation could be found.
		2. Which sectors are looking for data analysts? And which ones pay best?
			For the answer I dropped rows with missing values in the Sector column and calculated the count of job offers and the mean estimated salary per sector.
			The result is a list of sectors together with the job offers in this sector and the mean salary for it.
		3. Where are the most data analyst jobs offered? 
			After counting the job offers per location state, I created a plotly heatmap of the US which shows the number of job offers per state.
	- Evaluation
		The questions could be answered with the chosen method. However, the statements depend on the Glassdoor salary estimate. Should it turn out, that they are not accurate, they should be revised. Actual salary data would provide higher confidence.
	- Deployment
		The statistics are published in a Medium blog post https://medium.com/@tabeajanssen91/this-is-where-aspiring-data-analysts-should-look-for-their-new-flat-f03c0834a74a

5. Licensing, Authors, Acknowledgements, etc.
For license information please refer to the separate LICENSE file.

Thanks to https://www.kaggle.com/andrewmvd/data-analyst-jobs for providing dataset on Kaggle.
Banner image: https://www.chcf.org/blog/2020-race-revs-cnn-asks-americans-health-care/
