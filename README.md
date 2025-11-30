Bayesian optimization for predicting grain-boundary segregation in high-entropy alloys.

This repository contains the data and code for our recent work:

S. Das, N. Oyeniran, J. Walter, A. Gesch and C. Hu, Bayesian Opimization of Grain-Boundary Segregation in High-Entropy Alloys

The current repository demonstrates the implementation of the scalarization-based Bayesian optimization (SBO) to identify grain boundary (GB) segregation behavior in CrMnFeCoNi high-entropy alloys (HEAs). It contains two Jupyter notebooks:
1. Max_Segregation.ipynb – finds compositions/temperature that maximize Cr & Mn segregation and minimize Co, Ni, Fe segregation.
2. Min_Segregation.ipynb – finds compositions/temperature that minimize Cr & Mn segregation and maximize Co, Ni, Fe segregation.
Both notebooks use a Gaussian Process (GP) surrogate model with Thompson Sampling to explore the composition–temperature space and identify the optimal compositions that either enhance or suppress Cr/Mn segregation.

#Input Data
1. Max_Segregation/ANN_data.csv
2. Min_Segregation/ANN_data.csv
CSV file has these columns:
Inputs : Co_comp, Ni_comp, Cr_comp, Fe_comp, Mn_comp, Temp
Targets: Co_adsorption, Ni_adsorption, Cr_adsorption, Fe_adsorption, Mn_adsorption

#Running the code
1. Open the desired notebook (Max_Segregation.ipynb or Min_Segregation.ipynb) in Jupyter.
2. Make sure the file_path points to the correct ANN_data.csv.
3. Run all cells from top to bottom.

#Outputs
1. Optimal Composition and Temperature: Co, Ni, Cr, Fe, Mn, Temp.
2. Optimal combined score.
3. Uncertainty estimate from the GP model.
4. Predicted Cr and Mn adsorption at the optimum.
5. 3D plot: all data points (grey colored data points), sampled points during BO (turquoise), top-performing points near the optimum (purple).
6. Violin Plots (showing the composition distribution of the top-performing points)
   
