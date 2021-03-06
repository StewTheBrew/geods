# geods

GeoDS --- Geological Data Science are a bunch of functions ready to use in python 3.x environment. 

It aims to handle and classify 3D data coming from scanning (laser scanner, photoscans...) i.e. 3D point clouds - in order to study geomechanics starting from the
detection and the extraction of the main sets of discontinuities.

It includes 
- A normals computation file, that is a common simplified open3d http://www.open3d.org/docs/latest/index.html workflow, slightly improved, contained into 
  a single function. 
- A normals converter, which converts the normals matrix into dip and dip direction values for each point of the dataset.
- the IPDE (Iterative Pole Density Estimation), helpful to detect the main discontinuity sets of a rock mass. It is a statistical approach of evaluation with few 
  parameters input (explore the file if you are interested in using it, all you have to know to start a basic analysis is commented within).
- the SSE (Supervised Set Extraction), a single function that classifies the point cloud while it extracts discontinuity sets following the user input (again, 
  all you have to know to start the extraction is commented within the file).
- Automatic clustering techniques (K-Means and Gaussian Mixture) for a geological dataset.
- A small dataset with the results of the analysis (both plot and numeric) that refers to a part of a survey taken in Massa Lubrense (NA) from IdroGeo Srl. The file is subsampled because the entire file would be too large to be uploaded. This has normals and dip/dip direction computed with the method presented. To check it you can just delete these columns and repeat the functions. Plot and manual clustering is referred to the entire dataset. You can try to run the IPDE tweaking the parameters, results would be often the same on small point cloud like this. Also you can extract whatever set you want (most likely the ones identified) by using the SSE.
  
Be sure to first download all the dependencies needed including mplstereonet https://github.com/joferkington/mplstereonet to plot the results of your analysis.
Also in this module be sure to change the file stereonet_axes.py with the one provided here that has slight improvements

You can download the whole package or just copy the function(s) you need in the repository to use them and, perhaps, improve something.

All the work done and all possible contributions would be most likely included into a module ready to be directly installed. 
These functions, along with others, have been condensed into an embryonic software that goes by the same name (GeoDS). Therefore, the possibility of combining all the contributions for the benefit of the same and, one day, giving it a birth is not excluded.

All the functions and algorithms here are presented and discussed in a manuscript entitled "New methods for semi-automatic characterization of discontinuity sets from 3D point clouds: the Iterative Pole Density Estimation and the Supervised Set Extraction" by Stefano Cardia from Earth and Environmental Sciences Department (Aldo Moro University, Bari, Italy), Biagio Palma and Francesco Langella from IdroGeo Srl and Mario Parise, also from Earth and Environmental Sciences Department (Aldo Moro University, Bari, Italy).
