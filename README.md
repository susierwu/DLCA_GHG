# DLCA_GHG

Unlike static LCA calculation, the temporally dynamic LCA (DLCA) takes into account the temporal dynamics by calculating LCA on a pre-defined temporal scale (e.g., annual basis), through applying dynamic characterization factors (DCF) on a dynamic life cycle inventory (LCI).

This repo includes calculation of the DCF for GWP metrics of all GHGs following the IPCC Sixth Assessment Report (AR6). 

Data_input folder: 

- including a file of "hodnebrog20" used for calculating DCF of Halocarbons
 
- other files are LCI excel sheets that users enter dynamic LCI data. "LCI_TREE_input" is for the TreeExample, and "LCI_general_example" can be used for entering your own LCI data

Data_output folder: 

- This is the DCF output of CO2, CH4, N2O, as well as user-defined halocarbons, as calculated by the "1A/1B..." notebook 

Clone_chrisroadmap is cloned from "https://github.com/chrisroadmap/ar6" for modules in calculating DCF per AR6, effective radiative forcing (ERF) concept, as opposed to earlier RF concept.

Run the notebook in order: 
1. run "1A. " notebook for calculation of DCF for CO2, CH4, N2O (currently, it's already calculated and their DCF in the Data_output folder)
2. run "1B. " notebook for calculation of any of the user-defined halocarbons, the result will be saved to Data_output folder (currently, there's SF6 and CClF3 calculated as an example)

Once you have the DCF of all your project-related GHG calculated, prepare the dynamic LCI accordingly  (you can use the "LCI_general_example" sheet). 

Finally, run the notebook "2.DnyLCI_whDCF_GeneralCalc.ipynb" for final calculation of a DLCA. 
