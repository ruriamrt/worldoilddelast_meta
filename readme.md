Description:  
===========

The files in this repository can be used to replicate a meta-analysis of oil demand elasticities. Results from the metaregressions conducted as part of the analysis are used to produce baseline world oil demand elasticity estimates. 
Results from the meta-analysis were originally published in: Uria-Martinez, R., Leiby, P.N., Oladosu, G., Bowman, D.C., and Johnson, M.M. (2018). "Using Meta-Analysis to Estimate World Crude Oil Demand Elasticity". ORNL/TM-2018/1070.  
Available at: https://info.ornl.gov/sites/publications/Files/Pub120229.pdf  


R setup:
========
R version: R-4.2.2

R Studio version: RStudio 2022.12.0+353 "Elsbeth Geranium" Release (7d165dcfc1b6d300eb247738db2c7076234f6ef0, 2022-12-03) for Windows
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) RStudio/2022.12.0+353 Chrome/102.0.5005.167 Electron/19.1.3 Safari/537.36

Package versions:
- tidyverse 1.3.2  
- readxl 1.4.1  
- scales 1.2.1
- styler 1.9.1
- grid 4.2.2
- gridExtra 2.3
- stargazer 5.2.3
- knitr 1.41  
- tinytex 0.44
- broom 1.0.2
- broom.mixed 0.2.9.4
- car 3.1.1
- truncnorm 1.0.9  
- lmtest 0.9.40 
- sandwich 3.0.2
- multiwayvcov 1.2.3
- lme4 1.1.32
- ICC 2.4.0


Necessary files
================
Data:  

- oilddelasticity_db.xlsx: contains elasticity database to be used in the meta-analysis  
- auxiliary_inputs_20170829.xlsx: contains data needed to construct some of the moderator variables to be used in the metaregressions  

Analysis:  

- oildd_elast_metaanalysis_DataPrep_20170818.Rmd: reads and processes data and performs initial exploratory analysis  
- oildd_elast_metaanalysis_Stage1_20181120_Manuscript.Rmd: performs metaregression analysis and generates manuscript  



Steps for replication of the manuscript  
===========================================
Step 1: (if needed) Installing R, R Studio and any necessary R packages  
Step 2: Run oildd_elast_metaanalysis_DataPrep_20170818.Rmd (it will produce two output files that becomes the input files for the Stage1 .Rmd file)  
Step 3: Knit oildd_elast_metaanalysis_Stage1_20181120_Manuscript.Rmd to generate the manuscript ("oildd_elast_metaanalysis_Stage1_20181120_Manuscript.pdf")  
