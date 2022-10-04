# Abstract

Several variants for the retrieval of the thickness of thin sea ice was
proposed for space borne L-band radiometers such as {term}`SMOS`by ESA and {term}`SMAP` by NASA.
The algorithm presented here is based on the work of {cite}`huntemann2014` and works originally on intensity and polarization difference. In this ATBD the algorithm is modified to use directly instrument provided horizontal and vertical polarization, including their uncertainties. Another modification compared to {cite}`huntemann2014,Patilea2019` is the removal of a forced upper limit of 50cm of retrievable ice thickness. Higher ice thicknesses, even though retrieved, do come with higher uncertainties. The evaluation is done against the ESA CCI Round robin data package {cite}`Pedersen2021`.
{abbr}`
