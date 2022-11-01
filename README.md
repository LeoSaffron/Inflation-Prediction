# Predictiong and Analysis of Inflation

Hi,

My name is Leon, and this is my Analysis of inflation project.

In the project below I am going to analyze relationship between different inflation metrics, as well as predict price inflation.  

In the older days, the definition of inflation was increase of monetary supply, which devalues the currency.  
However in modern days by inflation what is meant usually in increase in prices, which also means devaluation of the currency, but in a different way.  

For the monetary supply index I will use M1 for this notebook.  
For the price index I will use CPI index,

In the nootebook below I am going to analyze the relationship between M1 and CPI as well as those indices individually.  

The final goal of the notebook is to build a model to predict CPI inflation index by data including the M1.

**Important note**  
There is a serious data drift in last 2 years due to covid,  
This notebook is focused on data prior to 2020 events.  

## Data description

### Monetary supply

There are various indices for measuring how much money exists in the economy:  
M0, M1, M2, M3, M4  
Basically the difference between them is what is considered as money in the index and what is not,  
For example M0 index is used to measure the amount of all banknotes and coins, and M1 adds checkable deposits (a type of credit) on top of that.  
each subsequent index includes more asset classes on top of what the previous one includes.  
More information on the indices:  
https://www.wallstreetmojo.com/money-supply/

All the data is available on the [Federal Reserve website](https://fred.stlouisfed.org/).  
We'll use the following dataset as it is not adjusted to inflation:  
https://fred.stlouisfed.org/series/M1NS  

### Prices increases

For the data for increases in prices we'll choose CPI (Consumer Price Index),  
It is calculated by the [U.S. BUREAU OF LABOR STATISTICS](https://www.bls.gov/).  
In short, it measures the cost of various specific goods that are consumed by everyday people.
Although this index is far from perfect for many reasons,  
It is still the most common index of prices inflation.  
More information on the CPI and how it is measured:  
https://www.investopedia.com/terms/c/consumerpriceindex.asp   

The data can be downloaded from the BLS website:  
https://www.bls.gov/cpi/data.htm  

### Glossary - important acronyms

**YoY** - Year-over-Year - means how the certain feature has changed compared to what it was exactly a year ago  
**MoM** - Month-over-Month - same concept as YoY, shows how the feature has changed compared a month ago  
**CPI** - Consumer Price Index (mentioned above) - measures increases in prices (price inflation)  
**M1, M2** - (mentioned above) different metrics to measure how much money is in the monetary system (monetary inflation)  

Please note that in this notebook we look at YoY and MoM as changes in percents, and not in raw values.