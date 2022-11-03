# Fundamentals of Agro-Environmental Data Science

# Exercise 7 - Find and use data online

This is an exploratory exercise, which should contribute to your portfolio of tools
for Data Science.

## Introduction

The availability of data online is comparable to an iceberg. What you see as a 
human can be only a fraction of all the data available. Even when data is not 
prepared to be served as a web service, it is possible to implement automatic
scripts (web scraping) that speed you data collection for reuse. But never forget 
the discussion about licencing that we had on class 06 
([slides](https://docs.google.com/presentation/d/1Grj-JJERGPorTKxtOcyLAcpAnWwbGHZ-8zXyS8bVnU4/edit?usp=sharing)).

In this exercise, we will learn how to get data available online. We will practice:
- to identify if data is provided by a web service (an API)
- how to recognise and use parameters of the web service to get specific data
- how to extract data from online pages that are not supported by a web service

## 1. Identify if an API is available

Not all data portals inform users that an API is available to serve data. Even when
there is, its identification is not done in the same way.

1. Portals with API services

The most recent and advanced platforms, developed with data service in mind,
make clear and easy to the normal user that an API is available.

For the following platforms, identify if an API is available. For each case, write
down:
- the path through menu/link navigation, from the home page to the information 
about an API availability (e.g. Home --> Data --> API)
- if there is documentation on how to use the API (take note of the URL link)
- an example URL that returns data provided by the API
- the format of data (json, xml, csv, several, ...)

| Platform | URL | Path to API information |Documentation URL | API URL | Data format |
|------|-----|-------------------------|------------------|---------|-------------|
| GBIF | https://www.gbif.org/ |   |   |   |   |
| Eurostat | https://ec.europa.eu/eurostat/ |   |   |   |   |
| INE | https://www.ine.pt/ |   |   |   |   |
| Climate Data Store | https://cds.climate.copernicus.eu/cdsapp#!/home |   |   |   |   |
| Copernicus Open Access Hub | https://scihub.copernicus.eu/ |   |   |   |   |
| WMO | https://worldweather.wmo.int/en/home.html |   |   |   |   |
| Agri4Cast | https://agri4cast.jrc.ec.europa.eu/DataPortal/ |   |   |   |   |
| European Environment Agency | https://www.eea.europa.eu/ |   |   |   |   |

2. (Optional) Repeat the analysis for data catalogues 

If you want, you can explore if the online catalogues of exercise 06 also have API
services (when appropriate):

- United Nations - UNDATA - http://data.un.org/ 
- UN partner organisations: http://data.un.org/Partners.aspx 
- FAO (several databases) - https://www.fao.org/statistics/databases/en/ 
- FAOSTAT - https://www.fao.org/faostat/en/#data 
- Copernicus Open Access Hub - Satellite data - https://scihub.copernicus.eu/ 
- European data - https://data.europa.eu/en 
- US Open Data - https://data.gov/
- Dados abertos da administração pública - Portugal - https://dados.gov.pt/pt/
- Data Portals - http://datacatalogs.org/
- Kaggle - online community - find and publish data sets - https://www.kaggle.com/   
- Google Data Search - https://datasetsearch.research.google.com/ 

## 2. Use web scraping

Many times, data is visually available in the web page, but no service is provided to 
download data. This does not mean that you have to obtain data manually, via a 
copy-paste approach, also because many times this would require a large effort.

Web scraping is the implementation of automatic scripts to extract data from 
websites. If you want to see an excellent article about how to do it with python, 
check [this example](https://realpython.com/python-web-scraping-practical-introduction/#extract-text-from-html-with-string-methods).

1. Develop a web scraping exercise

The QUALAR (https://qualar.apambiente.pt/) is a web platform of APA, the Portuguese Environment Agency, that displays online air quality data sampled by on air monitoring stations in Portugal. Unfortunately, the platform does not expose to the final user, or provides documentation how to use the API service that was implemented for web users downloads. Downloads are generated as XLSX files.

However, it is possible to hack the source code of the webpage to identify that there is an implemented API, and that it can be used to facilitate efficient download of data. 

In Jupyter Notebook, run the notebook [FADS Example02-apis](https://github.com/isa-ulisboa/greends-fads-jupyter/tree/main/example02-apis), that can be downloaded from [here](https://raw.githubusercontent.com/isa-ulisboa/greends-fads-jupyter/main/example02-apis/example-api.ipynb) (do ***Save as*** in your browser).

When you complete the exercise, answer/discuss the following questions:
- How can I detect that a web site has hidden data?
- When should I decide to do steps in web scraping manually ***versus*** doing everything
automatically?
- What advantages and problems do I have doing web scraping?
- What are the differences in getting data by between web scraping compared to an API? Which approach do I prefer and why?

2. Plan a web scraping exercise

Visit [SASSCAL WeatherNET](http://www.sasscalweathernet.org/index.php). Explore the details in data for one particular station of your choice.

Make a plan to scrap the information from this site:
- Can I do it (legally)? Why?
- Which items of information (IDs, parameters, etc) are available to use in web scraping?


## Wrap up
In this exercise, you learned about obtaining data from online sources in an automatic way:
- identify if API services are available
- understand web scraping
- plan for a web scraping implementation









