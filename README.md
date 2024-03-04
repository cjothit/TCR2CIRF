# TCR2CIRF
A MATLAB toolbox for estimation of connected instantaneous response functions (CIRFs) from travel time of catchment runoff. A detail description of the software can be found here:
https://doi.org/......

Description 
The CIRFs is defined as the probability density function of catchment runoff travel time.  This travel time is computed by summing the duration of water flow through surface, subsurface and open channel along its flow path, starting from its point of origin within the catchment or the hillslope and continuing until it reaches the outlet of the catchment.

The determination of CIRFs involves a multi-step flowchart and necessitates output results from the distributed hydrological model embedded in the software.  The software offers flexibility in terms algorithms, enabling exploration of the effects of different parameters and runoff generation processes.  

A MATLAB toolbox has been developed to replicate the functionality of hydrological processes in a transparent and adaptable manner.  Comprising seven primary functions representing distinct calculation steps, the toolbox features a modular architecture that facilitates easy modification.

1. Pixel topography
Function: Topo_cal.m/flow_dir.m
Input:       DEM data
Output:    Slope, Flow direction, pixel area accumulation


2. Climatic data time series
Function: Climate_gen.m/climate_timeseries.m
Input:      annual rainfall, number of storm, storm duration
Output:   time series of rainfall and potential evaporation


3. Infiltration excess runoff
Function: GreenAmpt_infiltration.m
Input:       soil parameters based on soil textures
Output:    HOF, Infiltration rate


4. Water balance for a pixel
Function: water_balance.m
Input:      climate, topography, soil, vegetation data
Output:   DOF, SSF, Evaporation


5. Travel time for surface runoff
Function: Traveltime_surface.m
Input:       HOF, DOF
Output:    Travel time to outlet for each pixels


6. Travel time for subsurface runoff
Function: Traveltime_subsurface.m
Input:       SSF
Output:    Travel time to outlet for each pixels


7. CIRFs calculation
Function: Catchment_CIRFs.m
Input:       Travel time to outlet for each pixels
Output:    CIRFs curve

System requirements
TCR2CIRF has been developed on a MATLAB R2018a, and earlier versions of MATLAB may not be supported. Only the base MATLAB installation is required, with no dependency on any of MATLAB's toolboxes.

Use
The samples folder contains an example script and data for running the workflow.

License
The code is licensed under GNU General Public License v3.0

TCR2CIRF: A MATLAB toolbox for estimation of connected instantaneous response function from travel time of catchment runoff.
by Chatchai Jothityangkoon
March, 2024

The TCR2CIRF software aims to provide a user-friendly tool for computing of catchment runoff travel time from a distributed hydrological model embedded in the software and defining the probability density function (IRF) of travel times of runoff along its flow path within the catchment.  This software incorporates the connectivity between different patches of runoff generation toward stream channel, leading to the definition of Connected IRFs (CIRFs). This software comprises seven main functions representing distinct calculations steps.

Requirements:
This software only requires a basic MATLAB setup.


Installation:
The software does not need any installation. It is sufficient to add the folders with subfolders to the MATLAB path.
Folder organization and quick start guide is included in TCR2CIRF Documentation file in documentation folder.

Please refer the article for more details
Chatchai Jothityangkoon: TCR2CIRF: A MATLAB toolbox for estimation of connected instantaneous response function from travel time of catchment runoff, SoftwareX, Vol.????
