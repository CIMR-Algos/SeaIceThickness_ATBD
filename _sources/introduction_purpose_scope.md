# Introduction, purpose and scope

This is a ATBD for a {term}`SIT` retrieval algorithm for {term}`CIMR`. The method
described here will use CIMR L1b brightness temperatures and
corresponding output will be L2b, i.e. swath based Sea Ice Thickness values in
original footprint coordinates of the L1b data product. For the retrieval only L-band brightness temperatures will be used in H and V polarization. Required information for the
retrieval include the {term}`TEC` and the {term}`TB` uncertainties. The
algorithm is based on the work of {cite}`Huntemann2014` and works originally on
intensity and polarization difference. In this ATBD the algorithm is modified
to use directly instrument provided horizontal and vertical {term}`TB` polarization,
including their uncertainties. 

This document is describing the algorithm and processing steps and the
processing of the L2b {term}`SIT` product. The document is intended for the
{term}`CIMR` users and parties interested in the details of the algorithm. It
is not intended to replace a product user guide.  For the first version of the
ATBD, the entire code is embedded in the corresponding notebooks. The code will
be separated from the notebooks in the future and will be distributed in the
"algorithm" directory of this repository.






