# MatPlotLib homework for GT Data Science Bootcamp
Use MatPlotLab in jupyter notebook to visualize data

## The task definition was given:

While your data companions rushed off to jobs in finance and government, you remained adamant that science was the way for you. 
Staying true to your mission, you've joined Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. 
In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.
As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. 
In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. 
Over the course of 45 days, tumor development was observed and measured. 
The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. You have been tasked by the executive team to generate all of the tables and figures needed for the technical report of the study. 
The executive team also has asked for a top-level summary of the study results.

### Analysis discussion

This data set had about 1900 data points for 249 mice that were given various treatments to test the efficacy of the treaments in reducing the size of tumors.  

The dataset contained:

    - Mouse ID which was the unique ID code for each mouse 
    - Timepoints for each tumor measurement - stated as an integer 
    - Tumor size for each data point in mm3
    - Drug Regimen
    - Gender Male/Female
    - Weight in grams
    - Metastatic Sites and Age_months were also provided but not used in this study


Intial data clean-up was done to evaluate the quality of the dataset. One mouse ID had duplicate entries for tumor-timepoints. This dubious data was removed from the list for the final efficacy analysis.

Bar charts were created to quickly look at the test points and determine if there were significant differences between the protocols.

Gender pie charts were rendered to show that the data points were close to evenly distributed across genders, thereby showing for this study no difference in outcomes based on gender. The gender distribution of the test points was 51% male and 49% female.

Regression was performed on mouse weight vs tumor size. A positive correlation exists. 

## Analysis : Conclusions based on the data 

####  Tumor volume has a positive correlation to mouse size

    1. Pearsons correlation was used to regress tumor volume vs mouse weight for the average tumor values for mice who were treated with the  Capomulin regimen. The pearsons correlation was 0.84 indicating a strong correlation
    2. Additional calculations need to be done across all mice to see if the corelation is equally strong across all treatment regimens tested

#### Capomulin and Ramicane showed markedly smaller tumor volumes  at the end of the study vs other treatment modalities
    
    1. Capomulin and Ramicane with mean tumors sizes at 40.22 and 40.68 respectively were 11-15 mm3 smaller than other drugs and vs placebo. A data table is displayed in the Summary Statistics section below enumerating the differences.
    2. A sample graph of tumor size over timepoints is shown in the attached analysis file for one mouse in the Capomulin regimen and another in the Ceftamin protocols. Aggregate data shows Ceftamin is ineffective at slowing tumor growth, Capomulin shows reductions in tumor size. 
   
    
#### Capomulin and Ramicane showed greater survival rates that other protocols

    - Capomulin and Ramicane had the highest quantity of data points in the study due to mouse fatalities for the other regimens including placebo. Although not shown in these results, there were 25 mice at the start in each protocol except Ketapril at 24. It is left to the reader to perform additional data steps if desired to see the fatalities vs drug regimen or other analysis.