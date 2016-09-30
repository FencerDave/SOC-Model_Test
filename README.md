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




    
    
  
