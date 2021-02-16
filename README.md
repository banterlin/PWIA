# Pressure-only wave intensity analysis.


For background see *Alun Hughes, Kim Parker. The modified arterial reservoir: an update with consideration of asymptotic pressure (P∞) and zero-flow pressure (Pzf). 
Proceedings of the Institution of Mechanical Engineers, Part H: Journal of Engineering in Medicine in press.* https://doi.org/10.1177/0954411920917557 and 
Kim Parker's website pages on Reservoir/excess pressure (http://www.bg.ic.ac.uk/research/k.parker/res_press_web/rp_home.html).



Main_vxx.m
This code used is for reservior-pressure analysis and Wave intensity computation 
for both conventional method and pressure only method.

This scrpit is designed to work for the resultant signals from data processing done by using Data_vxx.m

Default folder for data selection is 'C:\Spdata\' (This is also the directory that Data.m is storing data to).


%  v0.1 (First version working for virtual population1/2 with pulse and signal input)
%  v0.2 (** Removed code for calculating variables that are not considered in our study
%           Wave intensity calculation from Pxs.
%           automatic detection of last cardiac cycle from input of virtual population, so that we can use the last cardiac cycle(stable) to compute dI and dIxs
%  v0.3 


Data_vxx.m
Data processing to the virtual dataset. Each Txt files contained in the virtual popluation dataset 
consist of time [s], area [cm^2], velocity [cm/s], pressure [Pa / 100] and wave speed [cm/s].

The scrpit produce a new txt file that contains only the pressure and velocity waveform. This txt is then output to 'C:\Spdata\' .
Note the scrpit currently need to be placed in the directory of the raw dataset that you would like to analyse(i.e. C:\virtualpopluation\M\30-39\3).
