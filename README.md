# DensityEstimation
Matlab code for global thermospheric density estimation using two-line element data.

Disclaimer: This code is under development and may not directly run after installation. The code and instructions are being updated.

Installation instructions:
1. Download the DensityEstimation Matlab code
2. Download and install SPICE Toolkit for Matlab: https://naif.jpl.nasa.gov/naif/toolkit_MATLAB.html
3. Set the path to the SPICE Toolkit directory in mainDensityEstimation.m
4. Download SPICE kernels (i.e. ephemeris files): https://naif.jpl.nasa.gov/pub/naif/generic_kernels/ and put them in the folder Data. Download the following kernel files: naif0012.tls, de430.bsp, pck00010.tpc, MOD.tf, TOD.tf, earth_fixed.tf, earthstns_itrf93_050714.bsp, earth_070425_370426_predict.bpc, earth_720101_070426.bpc, earth_latest_high_prec.bpc
5. Download space weather file from Celestrak and put in folder Data: https://www.celestrak.com/SpaceData/SW-All.txt
6. Download Earth orientation data file from Celestrak and put in folder Data: https://www.celestrak.com/SpaceData/EOP-All.txt
7. Download 2 space weather files needed for the JB2008 model and put in folder Data: http://sol.spacenvironment.net/jb2008/indices/SOLFSMY.TXT  and  http://sol.spacenvironment.net/jb2008/indices/DTCFILE.TXT 
8. If you want to use automatic download of TLE data, then specify your “www.space-track.org” username and password in runDensityEstimationTLE.m. (Alternatively, you can download the TLE data manually and put them in the folder TLEdata with naming convention: NORADID.tle, e.g. 12388.tle )

Run instructions:
1. Open mainDensityEstimation.m
2. Specify the time window for density estimation by setting the start year, month and day and number of days
3. (Optionally) select the reduced-order density model and the reduction order (default r=10)
4. (Optionally) select the objects to use for density estimation
5. Run mainDensityEstimation


% David Gondelach, Sep 2019
% email: davidgondelach@gmail.com
