## Hello! 
This is all the code you will need to replicate my paper Three-Dimensional Empirical Orthogonal Functions Computed From An Ocean General Circulation Model: Mode Visualization and equatorial Upwelling. 

Here is a breakdown of what you will find in each folder:
  - OGCM: Contains all ogcm data needed te replicate all the plots in the paper, and one file of January OGCM data that is used to compute EOFs
      - Jan_ogcm.csv: January OGCM data used in 3D_EOF_Calc
      - aug_1990_OGCM.csv: August 1990 OGCM data used to plot figure 6c in code To plot all figures.ipynb
      - aug_2003_OGCM.csv: August 2003 OGCM data used to plot figure 6c in code To plot all figures.ipynb
      - aug_clim.csv: August climatology data used to plot figure 2b in code To plot all figures.ipynb
      - jan_1950_OGCM.csv: January 1950 OGCM data used to plot figure 1 in code To plot all figures.ipynb
      - jan_1993_OGCM.csv: January 1993 OGCM data used to plot figure 6b in code To plot all figures.ipynb
      - jan_2003_OGCM.csv: January 2003 OGCM data used to plot figure 6a in code To plot all figures.ipynb
      - jan_clim.csv: January climatology data used to plot figure 2 in code To plot all figures.ipynb
  - all Figures: Contains all figures from paper labeled according to paper
  - detrended_eigen: Contains all eigenvalues and eigenvectors computed from SVD and Temporal Covariance using detrended anomalies labeled as month_eval.csv or month_evec.csv.
      - Aug_evec.csv: August eigenvector data used to plot figure 14b and d in code To plot all figures.ipynb
      - Jan_evec: January eigenvector data used to plot figure 14a and c in code To plot all figures.ipynb
      - All eval files: eigenvalue data used to plot figure 13 in code To plot all figures.ipynb
  - eigen: Contains all eigenvalues and eigenvectors computed from SVD and Temporal Covariance (see 3D_EOF_Calc.ipynb) labeled as month_eval.csv or month_evec.csv. 
      - Aug_eval.csv: August eigenvalue data used to plot figure 3c  in code To plot all figures.ipynb
      - Aug_evec.csv: August eigenvector data used to plot figure 12a,d, and f in code To plot all figures.ipynb
      - Jan_eval: January eigenvalue data used to plot figure 3b in code To plot all figures.ipynb
      - Jan_evec: January eigenvector data used to plot figure 12a,c, and e in code To plot all figures.ipynb
      - All eval files: eigenvalue data used to plot figure 3a and fig 8 in code To plot all figures.ipynb
  - phys_EOFs: data of physical EOFs computed from 3D_EOF_Calc.ipynb
      - Aug_phys_EOFs.csv: August's physical EOFs used in various plots for To plot all figures.ipynb
      - Jan_phys_EOFs.csv: January's physical EOFs used in various plots for To plot all figures.ipynb
  - 3D_EOF_Calc.ipynb: Code used to compute 3D EOFs with SVD and temporal Covariance
  - To plot all figures.ipynb: Code to plot all figures in paper
  
  All codes are can be run on their own without having to download data. You may have an issue running the code if you do not have Basemap installed. Please be sure to install that prior to running the code
