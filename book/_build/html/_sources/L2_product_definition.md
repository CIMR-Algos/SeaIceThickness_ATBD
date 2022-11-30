# Level-2 product definition

The Level-2b product is the result of the processing from Level-1b brightness
temperatures to Level-2b ice thickness. The product is provided in the native
grid of the CIMR instrument at L-band frequency, which means it contains 135
samples per scan. Multiplied by the number of scans for each orbit gives the
number of retrieved ice thickness values per orbit. The product is provided in
NetCDF format and contains the following variables following the [CF
conventions](http://cfconventions.org/):

(product_variables)=
| variable name | description | unit | dimensions |
| --- | ---- | ---| ---- |
| `sea_ice_thickness` | mean ice thickness in given grid cell as per retrieval | m | n_scans * n_samples_earth |
| `sea_ice_thickness standard_error` | the standard error as described in {ref}`uncertainties` | m | n_scans * n_samples_earth |
| `sea_ice_thickness quality_flag` | product quality flag | 1 | n_scans * n_samples_earth| 


The dimension follow the definition of the original CIMR L1b product.

The quality flag is a 16-bit mask with the following bits:
(product_flags)=
| Bit | Description |
| --- | ---- |
| 0 | Validity of the retrieved ice thickness (set for valid) |
| 1 | Land mask (set for land) |
| 2 | Ice shelf mask (set for ice shelf) |
| 3 | Sea ice edge mask (set for sea ice edge) |
| 4 | full sea ice cover mask (set for sea ice concentration > 0.90) |
| 5-16 | Reserved |


The quality flag is an important indicator for users of the product. While for
full ice coverage of a grid cell the retrieval gives the best, i.e., lowest uncertainty sea ice thickness results,
the retrieval is still valid for lower ice concentrations. The sea ice edge mask is set
for grid cells where the retrieval is not valid due to the presence of the sea
ice edge. The ice shelf mask is set for grid cells where the retrieval is
not valid due to the presence of an ice shelf. The land mask bit is set for
grid cells where the retrieval is not valid due to the presence of land.
The validity of the retrieved ice thickness is set for grid cells where the
retrieval is valid in general, which is the major indicator for users of
the product.


