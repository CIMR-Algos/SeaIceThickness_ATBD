# Algorithm Input and Output Data Definition (IODD)

In order to process a swath of L2 SIT, the processing starts from a recent SIC
map (in swath projection). Land-mask information should be contained in the SIC
map. Land is removed before processing and while a flag for ice-free ocean can
be used, those pixels would be retrieved as 0 cm in any case. The input for the
ice thickness consists of $T_{b,h}$ and $T_{b,v}$ at 1.4 GHz and their
uncertainties NeΔT which are assumed Gaussian noise in this retrieval. The
corresponding output is thickness of thin sea ice up to 50 cm including the
uncertainty as described in this document. For retrieved values above 50 cm the
output will have the status flag for 50+ cm. 




## Input data

| Field | Description | Shape/Amount |
| ---   | ----------- | ------------ |
| L1B TB | L1B Brightness Temperature at L-band (both H and V polarization) | full swath or section of it (Nscans, Npos) |
| L1B NeΔT | Random radiometric uncertainty of the channels | full swath or section of it (Nscans, Npos) |
| sea-ice and land mask | A recent sea-ice concentration field including land information | SIC and land-mask collocated to swath. |

## Output data

| Field | Description | Shape/Amount |
| ----- | ----------- | ------------ |
| L2 SIT | Sea Ice Thickness | full swath or section of it (Nscans, Npos) |
| SIT uncertainty (4 fields) | Retrieval uncertainties: the total uncertainty as well as the 3 contributions separately. | full swath or section of it (Nscans, Npos) |
| Status Flag | A flag indicating status of retrieval, e.g. “nominal”, “over land”, “ice-free”, “50+cm” | full swath or section of it (Nscans, Npos) |

Note: over land areas, only the status flags will have a valid value, all the others will have “NaN” (_FillValue). Over ice-free ocean, the SIT will be 0 cm.


## Auxiliary data

Auxiliary data are used to improve the retrieval. They are not mandatory, but the retrieval will be
less accurate without them. This includes the {term}`TEC` for the transformation from {term}`TOA` to surface
brightness temperature.

## Ancillary data

Ancillary data includes the Masks for filling shelf and land areas. While Land areas are assumed
fixed, shelf ice is changing over time, in particular pronounced in the Antarctic. The shelf ice
mask is used to exclude shelf ice from the retrieval. The land mask is used to exclude land areas
from the retrieval.



