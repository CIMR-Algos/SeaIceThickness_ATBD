# Background and justification of selected algorithm


Over the course of the different L-band radiometers such as {term}`SMOS` and
{term}`SMAP`, several algorithms were proposed and implemented for the
retrieval of the {term}`SIT`.  {cite}`Tiankunze2014` presented an algorithm
which is used today in the ESA {term}`SMOS` official {term}`SIT` product. While
it is based on a combination of physical models, it provides similar {term}`SIT`
values to the empirical formulation from {cite}`Huntemann2014`, although,
extending the range of retrievable {term}`SIT` values up to 1m of ice thickness
for growing sea ice in freeze-up conditions.

Consequently, the algorithm used for CIMR {term}`SIT` retrieval is settled with
the empirical variant of {cite}`Huntemann2014`, but also extended to higher ice
thicknesses at increased uncertainty. Technically this is achieved by
considering a certain background ice thickness with a very low weight. Once the
sensitivity of brightness temperatures to thickness decreases in the thick ice
case, the weight on the background value is increased. This is done to avoid the
retrieval of unrealistically high ice thicknesses without artificially
constraining at a fixed boundary like in {cite}`Huntemann2014` and
{cite}`Patilea2019`. The algorithm is described in detail in {ref}`retrievalalgorithm`.
