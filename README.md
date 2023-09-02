# NetworkAnalysisProject
# Context
## General Context:
- Environmental Sciences
## Specific Applications:
- Greenhouse gas emissions analysis: Collection, analysis, and interpretation of data on 
CO2 emissions categorized by sector and country.
- Environmental Impact Assessment: Evaluation of CO2 emissions from specific sectors 
and countries.
# Problem and Motivation
The urgency of environmental concerns linked to global warming has escalated, presenting 
significant threats to the environment upon which human beings rely for their survival. Carbon 
emissions are a crucial aspect of both environmental and economic concerns. While it is 
essential to identify the factors that drive carbon emissions, it is also relevant to understand how 
the different roles of countries at a global level influence these emissions. 
Countries play diverse roles in the production of carbon emissions, and these roles may vary 
over time. It would be of interest to understand further their roles by examining their features in 
a network. Conclusions might point to ways for reducing emissions. Understanding the impact of 
country positions within global supply chains on carbon emissions would indeed be helpful in 
formulating effective strategies for reducing greenhouse emissions. By analyzing a network of 
CO2 emissions involving countries and sectors, we can discern the key factors contributing to 
emissions and explore the potential for improving emission reduction actions.
The objective of this project is to explore and interpret the characteristics of two networks in 
order to understand the relationships between countries and industrial sectors and identify any 
relevant patterns or groups of interest. Various Network Analysis measures will be applied to 
examine the characteristics of the network and identify relevant nodes and connections. The 
available data span from 1970 to 2022, allowing for comparisons between different analyses to 
obtain a more comprehensive picture. An analysis of two networks corresponding to different 
time periods will be therefore conducted to examine the evolution of country roles.
# Dataset
The project will use the IEA-EDGAR CO2 dataset, a component of the EDGAR (Emissions 
Database for Global Atmospheric Research) Community GHG database version 7.0 (2022). The 
dataset includes or is based on data from IEA Greenhouse Gas Emissions from Energy, available 
at www.iea.org/data-and-statistics , as modified by the Joint Research Centre.
EDGARv7.0 ( https://edgar.jrc.ec.europa.eu/dataset_ghg70#intro ) is the first product of the new 
EDGAR Community GHG emissions database, which is the outcome of an agreement between 
JRC and IEA to work more closely to gather to provide consistent harmonised CO2 emissions 
from fossil fuel combustion. It provides estimates for emissions of the three main greenhouse 
gases (CO2, CH4, N2O) and fluorinated gases per sector and country 
(https://edgar.jrc.ec.europa.eu/dataset_ghg70#p1 ).
For the purpose of this project, the considered data are the one regarding the CO2 emissions.
Networks
Two bipartite networks will be created, representing countries and industrial sectors at different 
points in time, with edges connecting each country to the industrial sectors responsible for their 
emissions. Edge weights will be based on the quantities of CO2 emissions per sector.
The results of the measures applications on the two networks will be compared to search for 
relevant differences in the selected time periods in order to highlight the changing of the 
emissions network features.
Measures
The following Network Analysis measures will provide a comprehensive perspective on the roles 
and importance of countries and sectors in the CO2 emissions network and their interactions. 
Centrality:
When calculating node centrality measures in bipartite networks, a possible approach is to 
apply PageRank on the one-mode projection of the network. However, the projection could
cause information loss and distort the network topology. Therefore, for better node ranking on 
bipartite networks, it has been chosen a ranking algorithm that fully accounts for the topology of 
both modes of the network. The BiRank package ( https://pypi.org/project/birankpy/ ), which 
implements bipartite ranking algorithms, will be used to perform the Pagerank on the bipartite 
Networks. (Reference: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8559594/ )
For performing the analysis it will also be taken into account the weighted nature of the 
networks. Therefore another centrality measure for weighted networks, the Laplacian centrality, 
will be computed through Networkx (reference:
https://www.sciencedirect.com/science/article/abs/pii/S0020025511006761 ).
Similarity :
Simrank measure performedwith Networkx will allow to provide insights into the degree of 
similarity between countries in their emissions behavior within shared industrial sectors, in 
order to identify similar countries and distinguish between the most impactful ones and the 
least impactful ones.
