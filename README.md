# Title: Modeling the Growth Dynamics of A20 murine leukemic cells 

Introduction 

Chronic Lymphocitic Leukemia (CLL) is the most common leukemia in adults typically affecting populations over 70 years old. CLL is marked by the uncontrolled growth of B lymphocytes.  It is not a particularly fatal type of leukemia but survival rates do decrease with age and other risk factors. It is also difficult to cure. Mathematical models have been used previously to simulate the behavior of cancer cells like death, growth, senescence, their interaction with other cells and their interactions with drugs. Modeling can also be used to simulate how cells may respond to a series or combination of treatments to determine the best course of treatment for specific cancers. The research group developed a model to simulate the growth dynamics of A20 murine leukemic cells with and without exposure to cancer drugs. They then carried out experiments for each of these conditions to fit their model to the data. A20 leukemic cells were used as a model for human cells. 

Experiments

The research group first observed the normal growth of the A20 cells in culture using Trypan Blue as a live/dead stain and counting the number of live cells every 12 hours using a hemocytometer. This was used to determine the growth rate parameter and the maximal cell population parameter. 
The group also assessed the cytotoxicity of different cancer drugs at different concentrations on the A20 cells. 
They then fit their simulated results to the ones they obtained from the experiments. 


Model 

Below is their model for the growth dynamics of the A20 cells without drug with parameters determined by their experimental data 

![plot](https://github.com/traceymoyston/CHE2410_Project2/blob/a9c3eed99829ae11c2872972dbbf00cad15a92f2/Screen%20Shot%202022-12-13%20at%2013.43.42.png)

Here A is the number of living cells in the culture at a specific time, Ad is the number of dead cells in the culture, r is the growth rate of the A20 cells (1/h) determined from experimenta, K is the maximal population of cells that can be present in the culture (cells/ml), μA is the death rate of the cells (1/h) and d is the rate of dissolution of the dead cells (1/h). 

The model was expanded to include the action of the drug on the cell growth dynamics 
![plot](https://github.com/traceymoyston/CHE2410_Project2/blob/a9c3eed99829ae11c2872972dbbf00cad15a92f2/Screen%20Shot%202022-12-13%20at%2013.43.50.png)

Here a new term has been added to each equation. C is the concentration of the drug, μAC is the cytotoxicity rate due to the drug (1/h), μCA is the deactivation rate of the drug as it kills the cells and this varies by drug (1/h) and μC is the chemical deactivation of the drug (1/h). 


Results and Implications 

![plot](https://github.com/traceymoyston/CHE2410_Project2/blob/647b0da8b1b7694feb765ea67bc00a14c5d2d59a/modelfit.png)
Fig.1 Model fitting to the data presented in the paper 

Figure 1 shows the model fitting to the experimental data using the model for the growth dynamics without drug. The starting live and dead cells were 50,000 and 2,500 cells, respectively. The simulated model generally fits the data and is similar to the simulated model presented in the paper, but not exactly. The parameters here were r = 0.07, K=4x10^6, d=0.017 and μA=3.73x10^-8.

Bifurcation analysis was done for the parameter μA looking at the state of living cells at the steady state of dead cells (2x10^6 cells). μA was chosen because it was thought that the death rate should have a great impact on the system growth dynamics and also 
![plot](https://github.com/traceymoyston/CHE2410_Project2/blob/c10022cc1228b745ee5f4511c90e3a0b3fe828c8/bifur.png)






![plot] (https://github.com/traceymoyston/CHE2410_Project2/blob/c10022cc1228b745ee5f4511c90e3a0b3fe828c8/Asens.png)


 

References 
Guzev E, Luboshits G, Bunimovich-Mendrazitsky S, Firer MA. Experimental Validation of a Mathematical Model to Describe the Drug Cytotoxicity of Leukemic Cells. Symmetry. 2021; 13(10):1760. https://doi.org/10.3390/sym13101760

