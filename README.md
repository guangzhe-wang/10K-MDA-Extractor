# 10K-MDA-Extractor

### What is *Management’s Discussion and Analysis of Financial Condition and Results of Operations* (*MD&A*) in 10 K filings?


“Management’s Discussion and Analysis of Financial Condition and Results of Operations”, item 7 in 10-K filings, gives the company’s perspective on the business results of the past financial year. This section, known as the MD&A for short, allows company management to tell its story in its own words. The MD&A presents:

- **The company’s operations and financial results**, including information about the company’s liquidity and capital resources and any known trends or uncertainties that could materially affect the company’s results. This section may also discuss management’s views of key business risks and what it is doing to address them.

- **Material changes** in the company’s results compared to a prior period.

- **Critical accounting judgments**, such as estimates and assumptions. These accounting judgments—and any changes from previous years—can have a significant impact on the numbers in the financial statements, such as assets, costs, and net income.

### Where can I obtain the raw 10-K/10-Q filings?


I recommend you to read this blog in which the author introduces three ways to obtain the filings. [How to Parse 10K and 10Q](https://yuzhu.run/how-to-parse-10x/) The code is based on the SEC suite in WDRS. 

- Download the filing information including cik code, company name, filing date, report date, file type, SEC official filing name, WDRS exclusive filing name from *List of Filings Exhibits* in WRDS SEC suite (SEC_suite_filing_info_test_sample.csv).
- Run download_filing_text.py in google colab and save all the raw 10-K/10-Q txt filings in your local PC.

### Extract *Item 7 MD&A* from raw 10-K/10-Q txt files


Use extract_mda.ipynb to extract MD&A. In the first step, use strict regular expression to extract MD&A, then in the step two, try to use easing regular expression to extract MD&A.


### Accuracy


In my dataset, I deal with 5679 10-K filings in the past 2 years and there are 206 MD&A that cannot be extracted after the two steps. In the demo, I deal with 163 10-K filings, and there are 16 filings that cannot be extracted.




