# Global CO2 Emissions Analysis

**Global CO2 Emissions Analysis** is a comprehensive data analysis tool developed for the Global Climate Action Consortium (a fictional organisation) to enable them to develop climate policies that are effective, equitable and globally coordinated. The Global Climate Action Consortium (GCAC) aims to monitor and evaluate national and regional progress toward emission reduction targets and empower member states with actionable insights for international negotiations and funding allocation. This tool should be useful to Data Scientists interested in climate analytics while the Dashboard will provide access to key insights for users from a non-technical background.

## Dataset Content
This project uses the [CO2 Emissions Dataset](https://www.kaggle.com/datasets/shreyanshdangi/co-emissions-across-countries-regions-and-sectors/data) from Kaggle, the dataset size is 13.1MB.<br>
The original data set has ~43k rows, but this analysis is conducted on <3k rows by focusing on country-level data and records from 1975 onwards.<br>
Analysis is performed on the following columns (carbon dioxide will be referred to as CO2):
| Purpose | Column name | Description |
| --- | --- | --- |
| Identifiers and Metadata | Name, iso_code, year | List of country names, ISO 3166-1 alpha-3 standard country code, observation year |
| Demographics and Economy | population, gdp, primary_energy_consumption | Country-wise population data and estimates, inflation-adjusted and cost-of-living–adjusted economic output across countries, energy use in terawatt-hours (TWh) |
| Total Emissions | co2, total_ghg | CO2 emissions land-use changes in million tonnes, total green house gas emissions |
| Per Capita & Efficiency Metrics | co2_per_capita, co2_per_gdp, energy_per_capita, energy_per_gdp | CO2 emissions and primary energy usage, per person (capita) and relative to economic output (gdp) |
| Sectoral Emissions | coal_co2, flaring_co2, gas_co2, oil_co2 | CO2 emissions from coal, gas flaring, gas and oil. Reported in million tonnes |
| Cumulative Measures | cumulative_co2 | Total accumulated CO2 emissions excluding land-use changes from earliest available year, expressed in million tonnes |

## How to use this tool
This project is developed and tested with Python 3.12.10.<br>
It is recommended to create a virtual environment before installing dependencies:

Run the following in the terminal:
```    
    python3.12 -m venv .venv
    source .venv/Scripts/activate
    pip install -r requirements.txt
```
The notebooks are designed to be ran and worked through in the following order:<br>
[01_data_etl](jupyter_notebooks\01_data_etl.ipynb)<br>
[02_statistics_and_visualisations](jupyter_notebooks\02_statistics_and_visualisations.ipynb)<br>
[03_ml_model](jupyter_notebooks\03_ml_model.ipynb)<br>
[CO2 Emissions Dashboard](dashboard\co2_emissions_dashboard.pbix) created using Power BI


## Business Requirements
As part of GCAC’s mission to drive equitable and data-informed climate policy, the following analytics capabilities are required to support strategic decision-making, international negotiations, and public engagement:

1. 📈 Emission Trend Monitoring<br>
Enable tracking of greenhouse gas emissions over time by country to evaluate progress toward climate goals and identify emerging risks.

2. 🔮 Emission Forecasting<br>
Support predictive modelling using regression and machine learning to simulate future emissions under various policy and economic scenarios.

3. 🌐 Cross-National Comparisons<br>
Provide comparative metrics such as per capita emissions, GDP-emissions ratios, and energy intensity to assess national performance and climate equity.

4. 🗺️ Global Climate Change Visualization<br>
Deliver intuitive visualizations that illustrate historical contributions to climate change and energy usage, enabling storytelling for policy, education, and advocacy.

## Hypotheses
* H1: Global average CO₂ emissions per capita have declined over the past decade, validated through linear regression test.
* H2: Energy consumption is positively correlated with both CO₂ and total GHG emissions across all countries, validated through correlation matrix.
* H3: Relationships between CO2 emissions, population and GPD explored through visualisations.

## Project Plan
* The dataset was chosen based on personal interest and importance in current affairs.
* Data was sourced from Kaggle before performing basic cleaning and exploration.
* Analysis and visualisations were created to answer the hypotheses and the data cleaning process was updated in light of changes needed to successfully complete these steps.
* Methodologies were chosen to best fit the business requirements and hypotheses.

## The rationale to map the business requirements to the Data Visualisations
1. Emission Trend Monitoring: total_ghg by year and country visualisation on Energy and Emissions dashboard page
2. Emission Forecasting: Linear regression ML model in Notebook 3
3. Cross-National Comparisons: Notebook 2 visualisations for hypothesis 1 and 3
4. Global Climate Change Visualization: Country Level Emissions dashboard page visualisations

## Analysis techniques used
* Data was analysed through a mix of statistical tests and visualisations, I would have liked to perform a correlation test for a more rigorous test of Hypothesis 2, but I did not have time.
* I tried to structure the analysis to take users on a journey through different climate metrics, starting with a simple look at changes over time and moving on to more complex interactions.
* The broadness of the dataset made it difficult to work with, I made decisions to narrow the focus on the analysis to make it more manageable.
* Generative AI was used throughout the ideation process and also as and aid with coding and summarising findings.<br>
  Full details of AI use in the project can be found in the [AI Usage Statement](AI_usage_statement.md)

## Ethical considerations
* The data contains country level information so there are no issues relating to personally identifiable information.
* The dataset is public domain so there are no issues with usage or sharing.
* There are ethical implications for the application of policies to reduce emissions, these may impact lower income members of the population who don't have access to sustainable energy sources,<br>
  there is also issues with restricting developing countries outputs when developed countries have benefited from historic emissions.

## Dashboard Design
All plots can be filtered by Year and Country to allow users to focus on specific areas of interest and compare subsets of data.
1. Energy and Emissions:
    * Linegraph showing CO2 by Year and Country
    * Linegraph showing Total GHG by Year and Country
    * Linegraph showing Primary Energy Consumption by Year and Country
2. Country Level Emissions:
    * Card showing selected country
    * Card showing Population in millions, GDP in $billions and Primary Energy Consumption in TwH for selected country
    * Pie chart showing CO2 generating energy sources for selected country
    * Line and stacked column chart showing cumulative CO2, total GHG and CO2 per capita by year for selected country
3. Summary: paragraph explaining key insights from the data
* Data insights are communicated through a technical audience through the tests and visualisations in notebook 2 as well as the Energy and Emissions page in the dashboard.<br>
  The latter allows users to drill down for specific country or time period information in the metrics. The Country Level Emissions page is aimed more towards a non-technical audience, with clean visuals<br>
  intended to provide an easy way to look at key metrics for the selected country. The Summary page is also aimed at these users, to provide key takeaways and offer areas of interest that they might<br>
  wish to explore further.
* The dashboard has a mix of complex and simple visualisations to help convey data insights to different audiences. 

## Conclusions
Global climate emissions is a complex but important area for analysis. Energy consumption and CO₂ emissions are heavily concentrated among a few major economies, mostly with high populations or<br>
economic outputs. That being said some countries have high GDP and energy use but low emissions, this probably reflects and increase in sustainable energy sources and this approach could be encouraged<br>
globally. Historic emissions data shows a greater output from developed countries in the past and it could be argued that they need to take greater responsibility for lowering global emissions<br>
as a whole, not only reducing their current emissions.

## Unfixed Bugs
* A bug was identified when trying to run the Y Data Profile Report, this has hopefully been fixed by changing the version of ipython but if users encouter the following error `ImportError: cannot import name 'display' from 'IPython.core.display'` this can be fix by installing ipython v7.23.1 by running the following command `pip install ipython==7.23.1` and restarting the notebook.
* The year value display for the linear regression graph in notebook 3 is based on a recalculated field for the ML model, this should have been converted back to the original format, but I did not have time.
* When I encountered gaps in my knowledge I used available resources to help me move forward, including LMS materials, web searches and generative AI.

## Development Roadmap
* I encountered several bugs during the etl phase which delayed my progress on other parts of the project<br>
  These were overcome through web search debugging and the use of integrated AI tool in vs code.
* Based on me project experience I would like to learn more about API integrations in data engineering.
There were two hypotheses which I didn't have time to test, but would make for interesting areas for further analysis:
* H4: Per capita CO₂ emissions are significantly higher in countries with smaller populations and high GDP.
* H5: Population growth is a stronger predictor of total GHG emissions than GDP growth in low-income countries.

## Main Data Analysis Libraries
* Pandas and Numpy: Used for database manipulation
* Matplotlib, seaborn and plotly: Used to create visualisations with the jupyter notebooks
* Statsmodels: Used for statistical analysis
* Scikit Learn and Yellow Bricks: Used for machine learning modelling
* Power BI for dashboard creation and interactive visualisations

## Credits 
* Thanks to my facilitator Emma Lamont for support and answering questions during the project
* Tool for importing user stories into GitHub by FaraiB: https://github.com/FaraiB/csv-to-github
* Various web sources (mostly Stack Exchange) for help with code debugging. These are detailed within the notebooks
* Harry Smithson for providing the project use information for our hackathon that I have adapted here

## Acknowledgements
* Thanks to Rachel Fallon for making me aware of the csv to github code and providing a version to handle additional import fields