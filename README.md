# SOC-Model_Test
Test Team's in-development version of the Aquion SOC Model

# Hello World
This repository is for development the SOC model and ofshoots/similar models. 
Users are encouraged to update the model whenever possible and to update the team whenever possible.

# Contents
SOC_Model.m
  Current revision of the completed Model.
SOC_Model.fig
  The accompanying GUI Figure, as called in SOC_Model.
  
# Project History
Currently the model is able to:
Accept two electron transfers for each electrode and build half-cell data (equal molarity for each)
Combine the two half-cells (each at a specified Capacity) to make a full cell.
    
Adjust each electrode's "Q Fade" by reducing available capacity.
Adjust the State-Of-Balance, shifting electrodes by a specified PERCENTAGE (not shifting Amp-hrs)
Calculate QV and IC curves for the currently displayed figures
Adjust chemistry for Temperature via NERNST equation
    
Create a VERY ROUGH impedance curve via a baseline ohmic portion and a reciporical (A/(B-x)) asymptotic function
Apply that impedance curve based on a user-entered current, to calculate the charge (or discharge) QV and IC curves. 
Allow the user to define the windows of the charge curves
    
Save the current dataset in an Excel file 
Allow the user to program in fade rates for each parameter, and a set iteration count. Apply the fade for each iteration and save as an Excel sheet. 
    
# LIST OF GOALS
### 0.0 Simple additions to compare to datasets

> 0.1) Include "# of Cells" parameter (4 for Battery, 32 for 8-stack, etc.) This is very straightforward but important, as our data is only comparable to the model if either it is scaled DOWN to 1-cell level, or the cells are Scaled upwards. 

> 0.2) Choose a default scale (Suggest: 2x2), and set all parameters to default to MATCH that data (aka expected Qloaded, typical Ref. cycle I, and typical BOL Impedance data). 

### 1.0 Design tool to compare EMPERICAL data to the model. 

> 1.1) Continue to improve the model and our assumptions to increase the accuracy of the model. 

> 1.2) Identify situations inwhcih the model fails to match data, and address these issues 

> 1.3) Eventually, Use the fitting parameters of a dataset to more complexly describe that battery's State-of-Health! 

>> 1.3.1) Follow-on: automate fitting algorythm to accept larger datasets (CSV of reference cycles?) and output fit parameters for each curve.

### 2.0 Design tool to SIMULATE TESTS based on fade parameters
(Already slightly implimented in 'Save/Automate' Panel, but there is a great opportunity to expand this tool in different Areas)

> 2.1) Manually Input Cycling Parameters (Current, Voltage, Capacity, etc.) and limits, and generate a CONTINUOUS dataset based on the model. 

>> 2.1.1) Output this dataset, possibly in DATA_EXTRACTOR Readable format??> (Discuss.. This may end up as MISLEADING 'DATA' which must be avoided on a company-level)

>> 2.1.2) Input Cycling Parameters in the form of a CSV OF A MACCOR SCRIPT! in order to DIRECTLY compare model data to actual testing data. 

> 2.2) Input Fade Parameters to generate continuous datasets which include battery fade.

>> 2.2.1) Begin with BASIC {'per cycle', 'per throughput, or 'per day'} Fade Parameters (as in the existing save/automate panel) 

>> 2.2.2) Allow for Triggered or Calculated fade Parameters based on lifetime data (Example 1: SOB Fading 1% for every 100Ahrs spent above 2.0 Volts/cell) (Example 2: Impedance Z-factor begins to grow as a quadratic (instead of linear) after daily Q cycles begin to hit TOC limits)... There is a nearly infinite array of possibilities to model here, so discression will be very important to avoid losing focus. 


    
    
  
