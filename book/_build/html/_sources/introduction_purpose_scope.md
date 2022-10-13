# Introduction, purpose and scope

This is a ATBD of {cite}`SIT` retrieval algorithm for {term}`CIMR`. It method
described supposed to act on the CIMR L1b brightness temperatures and
corresponding output will be L2b, i.e. Swath based brightness temperature in
original footprint coordinates. For the retrieval only L-band brightness
temperatures will be used in H and V polarization. Required information for the
retrieval include the {term}`TEC` and the {term}`TB` uncertainties. The
algorithm is based on the work of {cite}`huntemann2014` and works originally on
intensity and polarization difference. In this ATBD the algorithm is modified
to use directly instrument provided horizontal and vertical polarization,
including their uncertainties. 

This document is describing the algorithm and processing steps and the
processing of the L2b {term}`SIT` product. The document is inteded for the CIMR
users and interested parties. It is not intended to replace a product usere
guide. The algorithm is implemented in the {term}`SIT` retrieval software
package which is distributed in the "algorithm" directory of this repository.



