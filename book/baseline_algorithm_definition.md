# Baseline Algorithm Definition

The sea ice thickness (SIT) retrieval algorithm is based on the algorithm
described in RD-3, RD-4 and {cite}`Huntemann2014`. It is an empirical
algorithm based on modeled ice thicknesses during the freeze-up in the Kara-
and Barents Seas. The underlying physical principle is the penetration depth of
L-band radiation into sea ice and the resulting correlation of the emitted
radiation to ice thickness.



### Forward Model
The algorithm ({cite}`Huntemann2014`) was initially introduced for the SMOS
(Soil Moisture Ocean Salinity) mission for an incidence angle range of 40°-50°
and is adapted here to the CIMR incidence angle of 55° using the fitting
procedure for horizontal and vertically polarized radiation presented in RD-4.
With these, the intensity $I=T_{b,h} \cdot T_{b,v} \cdot 0.5$ and the polarization
difference $Q=T_{b,v}−T_{b,h}$ is calculated. Analogous to RD-3, the SMOS data in the
training areas in the Kara and Barents Seas are used and the relations of
Intensity and Polarization difference is fitted using a least square fit with 7
parameters in total:

```{math}
:label: intensity_sit
I(a,b,c,x)=(a−(a−b)\exp(−x/c)
```

```{math}
:label: poldiff_sit
Q(d,e,f,g,x)=(e−(e−d)\exp(−(x/f)^g)
```

Where x is the ice thickness in cm, and a to g are the fitting parameters. The
parameters resulting from the least square fit of SMOS data are given in Table {ref}`parameterstab`.

```{table} Parameters for forward model 
:name: parameterstab

| Parameter | a | b | c | d | e | f | g |
| ---- | --- | --- | --- | --- | --- | --- | --- |
| Value | 232.2 | 108.3 | 13.4 | 33.8 | 81.2 | 33.7 | 1.64 |
```

### Retrieval Method

The functions {eq}`intensity_sit` and {eq}`poldiff_sit` are serving as forward model which inverse is then the retrieval function

```{math}
:label: inversion
x_{retrieved} = argmin_{x\in \mathcal{R} >0} \left((I_{fw}(x) -I_{obs})^2 +(Q_{fw}(x) - Q_{obs})^2 \right)
```


### Algorithm Assumptions and Simplifications

Subsection Text

### Level-2 end to end algorithm functional flow diagram


### Functional description of each Algorithm step

Subsection Text

##### Mathematical description

SubSubsection Text
##### Input data

SubSubsection Text

##### Output data

SubSubsection Text

##### Auxiliary data

SubSubsection Text

##### Ancillary data

SubSubsection Text

##### Validation process

SubSubsection Text


