# Measuring Temporal Concentration: An Application to Travel Demand Imbalance on London Underground

## Abstract of Research

One of the challenges in the planning and management of urban transport networks is the imbalance in travel demand at different locations or times of the day. The spatial and temporal concentration of travel demand can have implications for the operations, finances and user experience of urban transport networks. It is therefore imperative to understand these patterns by taking a quantitative approach for the analysis of the concentration of travel demand.

The Gini index has been used before as a measure of variability. In this research, it is argued that the Gini index can also be used as a measure of the spatial or temporal concentration of a phenomenon, such as the number of commuters passing through a certain station in the transport network. However, the Gini index is not sensitive to the spatial or temporal dependencies in the data. Hence, two scenarios with different level of dependencies can yield the same value of the Gini index. While there have been efforts to quantify the contribution of spatial dependencies to the measure of spatial concentration, such approaches have not yet been applied to the temporal context.

The aim of this research is therefore to develop a method for quantifying the temporal concentration and the contribution of temporal dependencies of a given phenomenon. This method was used to quantify the temporal concentration of travel demand on an urban transport network through the case study of London Underground. Machine Learning techniques were then used to identify features that influence the temporal concentration of travel demand and cluster stations based on their similarities in these features. Finally, the effectiveness of this method in detecting changes in travel patterns was tested to distil important learning points. 

## Info about Github Repository

This Github repository contains the code used for the analysis in this research and the outputs. The iPython notebooks are numbered in sequence according to the research workflow. A description of the notebooks is provided below.

|Notebook      |Description   |
|--------------|--------------|
|01-data-prep |Explore data provided by TfL and prepare demand profile for all stations for subsequent analysis |
|02-measure-development |Select the temporal weight matrix for computing Gini correlation, and compute Gini index and Gini correlation for all stations |
|03-significance-test |Test the significance of Gini index and Gini correlation using Monte Carlo simulations and permutation tests respectively |
|04-feature-selection |Use Random Forest to identify features that influence Gini index and Gini correlation |
|05-clustering |Use K-Means clustering algorithm to cluster stations based on their similarity in the features |
|06-covid |Test whether Gini index and Gini correlation can detect changes in travel patterns using Covid-19 pandemic as a test case |

All data used in this research were not provided in this repository as they were either provided by third party specifically for the purpose of this research only, or available on open data sources. A brief description of the data is provided below, along with the sources.

|Dataset       |Description   |Source        |Date Accessed |
|--------------|--------------|--------------|--------------|
|tfl_data |Data on the journey on London's rail network between January 2020 and October 2021 |Data provided by TfL specifically for the purpose of this project only. Similar data on travel demand is available at TfL's open data portal. ([http://crowding.data.tfl.gov.uk/](http://crowding.data.tfl.gov.uk/)) |N.A. |
|AC2021_ByQhrEntryExit.xlsx |Data on entries and exits at stations. Used to identify London Underground stations and operating hours in this dissertatio.n |[http://crowding.data.tfl.gov.uk/](http://crowding.data.tfl.gov.uk/) |19 May 2022 |
|land_use_2018.xlsx |Land use data at LAD-level in 2018. Used for feature selection. |[https://www.gov.uk/government/statistical-data-sets/live-tables-on-land-use](https://www.gov.uk/government/statistical-data-sets/live-tables-on-land-use) |21 July 2022 |
|lsoa_pop_density_mid2020.xlsx |Population density at LSOA-level in 2020. Used for feature selection. |[https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/datasets/lowersuperoutputareapopulationdensity](https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/datasets/lowersuperoutputareapopulationdensity)| 21 July 2022|
|lsoa_jobs_count_2020.csv |Jobs count at LSOA-level in 2020. Used for feature selection. |[https://www.nomisweb.co.uk/query/construct/summary.asp?mode=construct&dataset=189&version=0](https://www.nomisweb.co.uk/query/construct/summary.asp?mode=construct&dataset=189&version=0) |21 July 2022 |
|naptn.csv |Locations of National Public Transport Access Nodes. Used for feature selection. |[https://www.data.gov.uk/dataset/ff93ffc1-6656-47d8-9155-85ea0b8f2251/national-public-transport-access-nodes-naptan](https://www.data.gov.uk/dataset/ff93ffc1-6656-47d8-9155-85ea0b8f2251/national-public-transport-access-nodes-naptan) |21 July 2022 |
|lad_boundaries.zip |Boundaries of Local Authority Districts. Used for mapping and data aggregation for feature selection. |[https://geoportal.statistics.gov.uk/datasets/fef73aeaf13c417dadf2fc99abcf8eef/explore?layer=0&location=51.640057%2C-0.511728%2C10.50](https://geoportal.statistics.gov.uk/datasets/fef73aeaf13c417dadf2fc99abcf8eef/explore?layer=0&location=51.640057%2C-0.511728%2C10.50) |21 July 2022 |
|lsoa_boundaries.zip |Boundaries of Lower Super Output Areas. Used for mapping and data aggregation for feature selection. |[https://geoportal.statistics.gov.uk/datasets/ons::lower-layer-super-output-areas-december-2011-boundaries-generalised-clipped-bgc-ew-v3/explore?location=52.883172%2C-5.454967%2C9.99](https://geoportal.statistics.gov.uk/datasets/ons::lower-layer-super-output-areas-december-2011-boundaries-generalised-clipped-bgc-ew-v3/explore?location=52.883172%2C-5.454967%2C9.99) |21 July 2022 |
|central_activities_zone.gpkg |Boundaries of Central Activities Zone. Used for mapping and data aggregation for feature selection. |[https://data.london.gov.uk/dataset/central_activities_zone](https://data.london.gov.uk/dataset/central_activities_zone) |21 July 2022 |