# 3D EOF Computation
Program by: Danielle Lafarga\
Program created as part of NERTO project in May 2021

The following code is used to compute EOFs using temporal covariance. The program already assumes that the data had been read in and formated to a N by y data matrix called data_T where N is the total number of grid points (Lat x Long x Depth) and Y is the total amount of time steps. The process then goes as follows:

1. Climatology, standard deviation, and anomalies are computed from data_T 
2. Area weights are added to the anomaliies 
3. Temporal covariance is computed from the weighted anomalies. 
    -Note: it is important that prior to computing covariance the weighted anomalies are rid of NaNs and in a matrix that is N' by Y where N' is the new number of gridpoints without NaNs. 
4. Eigenvalues and eigenvectors are computed from temporal covariance
5. EOFs are computed using
<div align="center">
$EOF =\frac{A \vec{v}}{norm(A \vec{v})} $


    where:
        - EOF are the EOFs in a N by Y matrix where each column is the mode
        - A are the weighted anomalies in an N by Y matrix 
        - v are the sorted eigenvectors of shape 1 by N computed from temporal covariance

Important Variables:
- N: total number of grid points. Should be 
    - $N = latitude \times longitude \times depths$
- Y: total number of time steps. For example if data is taken monthly for 54 years then Y = 54 as this is only done for the respective month. 
- data_T: N by Y matrix with data
- clim_sdev: N by 2 marix with CLimatology and Standard deviation in the first and second column respectively 
- anom: N by Y matrix with anomalies
- stnd_anom: N by Y matrix with standardized anomalies
- x: Longitutde values
- y: Latitude values 
- area_weight: N by 1 array with area weights 
- cov: temporal Covariance Y by Y matrix
- eigvecs: eigenvectors computed from cov. These are all put into a matrix of size Y by Y with every column as the eigenvector
- ev: eigenvectors computed from cov. These are all put into a matrix of size Y by Y with every row as the eigenvector
- eigvals: eigenvalues computed from cov. 
- EOF: N by Y EOF matrix where every column is the mode 


the entire break down of the code can be found on https://dlafarga.github.io/journal/Covarianceintime.html
This includes the proof for this computation. If you have any further questions please reach out to me at dlafarga9505@sdsu.edu
