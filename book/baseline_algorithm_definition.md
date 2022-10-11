# Baseline Algorithm Definition

The sea ice thickness (SIT) retrieval algorithm is based on the algorithm
described in RD-3, RD-4 and {cite}`Huntemann2014`. It is an empirical
algorithm based on modeled ice thicknesses during the freeze-up in the Kara-
and Barents Seas. The underlying physical principle is the penetration depth of
L-band radiation into sea ice and the resulting correlation of the emitted
radiation to ice thickness.



## Forward Model
The algorithm ({cite}`Huntemann2014`) was initially introduced for the SMOS
(Soil Moisture Ocean Salinity) mission for an incidence angle range of 40°-50°
and is adapted here to the CIMR incidence angle of 53° using the fitting
procedure for horizontal and vertically polarized radiation.
The SMOS data in the training areas in the Kara and Barents Seas are used and the relations of
Intensity and Polarization difference is fitted using a least square fit with 6
parameters in total:

```{math}
:label: intensity_sit
I(a,b,c,x)=(a−(a−b)\exp(−x/c)
```

Where x is the ice thickness in m, and a to g are the fitting parameters. The
parameters estimated from the least square fit of SMOS data are given in {numref}`retrieval parameters`.
The derivation of the forward model parameters is outlined in {numref}`fw-model`.




