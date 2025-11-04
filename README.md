# Global CO2 Emissions Analysis

**Global CO2 Emissions Analysis** is a comprehensive data analysis tool designed to enable exploration of global CO2 emissions data, and provide analysis and visualisations to understand global emission trends. The tool provides an intuitive interface for both novice and expert data scientists.

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
| Per Capita & Efficiency Metrics | co2_per_capita, co2_per_gdp, consumption_co2_per_capita, consumption_co2_per_gdp, energy_per_capita, energy_per_gdp | CO2 emissions, consumption-based emissions and primary energy usage, per person (capita) and relative to economic output (gdp) |
| Sectoral Emissions | cement_co2, coal_co2, flaring_co2, gas_co2, land_use_change_co2, oil_co2, trade_co2 | CO2 emissions from cement, coal, gas flaring, gas, land-use changes, oil and trade. Reported in million tonnes |
| Global Share Indicators | share_global_cement_co2, share_global_co2, share_global_co2_including_luc, share_global_coal_co2, share_global_flaring_co2, share_global_gas_co2, share_global_luc_co2, share_global_oil_co2, trade_co2_share | Proportion of worldwide CO2 emissions by sector, expressed as a percentage |
| Cumulative Measures | cumulative_co2, cumulative_co2_including_luc, share_global_cumulative_co2 | Total accumulated CO2 emissions excluding and including land-use changes from earliest available year, expressed in million tonnes and percentage of global cumulative emissions excluding land-use changes since first year of recorded data |
| Temperature Change Attribution | share_of_temperature_change_from_ghg, temperature_change_from_co2, temperature_change_from_ghg | Proportion of global temperature rise attributed to green house gases as a percentage, increase in average global temperature due to CO2 and all green house gases measued in °C |

## Business Requirements
* Describe your business requirements<br>
* Track emission trends over time by country or region
* Forecast future emissions using regression or machine learning models
* Compare per capita emissions, GDP-emissions ratios, and energy use across nations
* Examine the role of trade and land-use change in emissions
* Use temperature change estimates to assess climate responsibility
* Visualize contributions to global climate change over time*

## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 

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