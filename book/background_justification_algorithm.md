# Background and justification of selected algorithm


Over the course of the different L-band radiometers such as {term}`SMOS` and {term}`SMAP`, several different algorithms were proposed and implemented for the retrieval of the {term}`SIT`. 
{cite}`Tiankunze2014` presented an algorithm which is used today in the ESA {term}`SMOS` official {term}`SIT` product. While it is based on a combination of physical models, it provides similar {term}`SIT` values to the empirical formulation from {cite}`Huntemann2014`, allthough, extending the range of retrievable {term}`SIT` values up to 1m of ice thickness for growing sea ice in freeze-up conditions.

Consequently, the algorithm used for CIMR {term}`SIT` retrieval is setteled with the emperical variant of {cite}`Huntemann2014`, but also extended to higher ice thicknesses at increased uncertainty. Technically this is achieved by assuming a certain background ice thickness, which has a low weight on the retrieved ice thickness, but enough to prevent it from divergence.
