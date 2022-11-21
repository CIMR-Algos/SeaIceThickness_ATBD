# Baseline Algorithm Definition

The basic idea of the sea ice thickness (SIT) retrieval algorithm is based on the algorithm
described in RD-3, RD-4 and {cite}`Huntemann2014`. It is an empirical
algorithm based on modeled ice thicknesses during the freeze-up in the Kara-
and Barents Seas. The underlying physical principle is the penetration depth of
L-band radiation into sea ice and the resulting correlation of the emitted
radiation to ice thickness. In the following the fitting of the forward model is described, followed by the algorithm itself.