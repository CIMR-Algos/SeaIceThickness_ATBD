# Level-2 product definition

The Level-2b product is the result of the processing from Level-1b brightness
temperatures to Level-2b ice thickness. The product is provided in the native
grid of the CIMR instrument at L-band frequency, which means it contains 135
samples per scan. Multiplied by the number of scans for each orbit gives the
number of retrieved ice thickness values per orbit. The product is provided in netCDF format and contains the
following variables following the [CF conventions](http://cfconventions.org/):

(product_variables)=
| Variable name | Unit | dimensions |
| --- | ---- | ---| 
| `sea_ice_thickness` | m | n_scans * n_samples_earth |
| `sea_ice_thickness standard_error` | m | n_scans * n_samples_earth |
| `sea_ice_thickness quality_flag` | 1 | n_scans * n_samples_earth| 


The dimension follow the definition of the original CIMR L1b product.

The quality flag is a 8-bit mask with the following bits:
(product_flags)=
| Bit | Description |
| --- | ---- |
| 0 | Validity of the retrieved ice thickness (set for valid) |
| 1 | Landmask (set for land) |
| 2 | Ice shelf mask (set for ice shelf) |
| 3-8 | Reserved |

