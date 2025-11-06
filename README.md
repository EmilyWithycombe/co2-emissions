# Global CO2 Emissions Analysis

**Global CO2 Emissions Analysis** is a comprehensive data analysis tool developed for the Global Climate Action Consortium (a fictional organisation) to enable them to develop climate policies that are effective, equitable and globally coordinated. The Global Climate Action Consortium (GCAC) aims to monitor and evaluate national and regional progress toward emission reduction targets and empower member states with actionable insights for international negotiations and funding allocation. This tool should be useful to Data Scientists interested in climate analytics while the Dashboard will provide access to key insights for users from a non-technical background.

## Dataset Content
This project uses the [CO2 Emissions Dataset](https://www.kaggle.com/datasets/shreyanshdangi/co-emissions-across-countries-regions-and-sectors/data) from Kaggle, the dataset size is 13.1MB.<br>
The original data set has ~43k rows, but this analysis is conducted on <10k rows by focusing on country-level data and records from 1975 onwards.<br>
Analysis is performed on the following columns (carbon dioxide will be referred to as CO2):
| Purpose | Column name | Description |
| --- | --- | --- |
| Identifiers and Metadata | Name, iso_code, year | List of country names, ISO 3166-1 alpha-3 standard country code, observation year |
| Demographics and Economy | population, gdp, primary_energy_consumption | Country-wise population data and estimates, inflation-adjusted and cost-of-living–adjusted economic output across countries, energy use in terawatt-hours (TWh) |
| Total Emissions | co2, co2_including_luc, consumption_co2, total_ghg | CO2 emissions excluding land-use changes, including land-use changes and based on national consumption in million tonnes, total green house gas emissions |
| Emission Growth Metrics | co2_growth_abs, co2_growth_prct | Yearly total and percentage increase in CO2 emissions, excluding land-use changes |
| Per Capita & Efficiency Metrics | co2_per_capita, co2_per_gdp, energy_per_capita, energy_per_gdp | CO2 emissions and primary energy usage, per person (capita) and relative to economic output (gdp) |
| Sectoral Emissions | cement_co2, coal_co2, flaring_co2, gas_co2, land_use_change_co2, oil_co2 | CO2 emissions from cement, coal, gas flaring, gas, land-use changes and oil. Reported in million tonnes |
| Global Share Indicators | share_global_cement_co2, share_global_co2, share_global_co2_including_luc, share_global_coal_co2, share_global_flaring_co2, share_global_gas_co2, share_global_luc_co2, share_global_oil_co2 | Proportion of worldwide CO2 emissions by sector, expressed as a percentage |
| Cumulative Measures | cumulative_co2, cumulative_co2_including_luc, share_global_cumulative_co2 | Total accumulated CO2 emissions excluding and including land-use changes from earliest available year, expressed in million tonnes and percentage of global cumulative emissions excluding land-use changes since first year of recorded data |

## Business Requirements
As part of GCAC’s mission to drive equitable and data-informed climate policy, the following analytics capabilities are required to support strategic decision-making, international negotiations, and public engagement:

1. 📈 Emission Trend Monitoring<br>
Enable tracking of greenhouse gas emissions over time by country to evaluate progress toward climate goals and identify emerging risks.

2. 🔮 Emission Forecasting<br>
Support predictive modelling using regression and machine learning to simulate future emissions under various policy and economic scenarios.

3. 🌐 Cross-National Comparisons<br>
Provide comparative metrics such as per capita emissions, GDP-emissions ratios, and energy intensity to assess national performance and climate equity.

4. 🔄 Trade and Land-Use Impact Analysis<br>
Analyze the role of international trade and land-use changes in shifting emissions across borders, highlighting indirect contributions and policy blind spots.

5. 🌡️ Climate Responsibility Attribution<br>
Use temperature change estimates to quantify national contributions to global warming, supporting climate justice and accountability frameworks.

6. 🗺️ Global Climate Change Visualization<br>
Deliver intuitive visualizations that illustrate historical and projected contributions to climate change, enabling storytelling for policy, education, and advocacy.

## Hypothesis [and how to validate]?
* H1: Global average CO₂ emissions per capita have declined over the past decade, validated through linear regression test.
* H2: Energy consumption is positively correlated with both CO₂ and total GHG emissions across all countries, validated through correlation test.
* H3: Rapid GDP growth is positively correlated with increases in total GHG emissions in developing nations.
* H4: Per capita CO₂ emissions are significantly higher in countries with smaller populations and high GDP.
* H5: Population growth is a stronger predictor of total GHG emissions than GDP growth in low-income countries.

## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Conclusions

## Unfixed Bugs
* A bug was identified when trying to run the Y Data Profile Report, this has hopefully been fixed by changing the version of ipython but if users encouter the following error `ImportError: cannot import name 'display' from 'IPython.core.display'` this can be fix by installing ipython v7.23.1 by running the following command `pip install ipython==7.23.1` and restarting the notebook.
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* Tool for importing user stories into GitHub by FaraiB: https://github.com/FaraiB/csv-to-github



## Acknowledgements
* Thanks to Rachel Fallon for making me aware of the csv to github code and providing a version to handle additional import fields