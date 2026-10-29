# Third-party code notices

Original code developed for DREAM is licensed under the MIT License, copyright
(c) 2025 Daijun Zhang. Third-party portions remain subject to their respective
licenses and copyright notices. DREAM imposes no additional access or use
restrictions beyond the applicable licenses.

## STAGATE and STAGATE_pyG

- Copyright (c) 2021 Kangning Dong.
- License: MIT License; see [complete license text](licenses/STAGATE-LICENSE.txt).
- Original STAGATE implementation:
  https://github.com/QIFEIDKN/STAGATE/blob/main/STAGATE/utils.py
- STAGATE_pyG implementation:
  https://github.com/RucDongLab/STAGATE_pyG/blob/main/STAGATE_pyG/utils.py
- DREAM location: `DREAM/DREAM_stage1/utils.py`.
- Verified corresponding portions: the first definition of `Cal_Spatial_Net`,
  `Stats_Spatial_Net`, and `Transfer_pytorch_Data`.

The first two functions correspond to the original STAGATE implementation;
`Transfer_pytorch_Data` corresponds to STAGATE_pyG. The reviewed implementations
have the same Python syntax trees after excluding documentation strings.
The DREAM file also contains a later definition of `Cal_Spatial_Net`; this
verified mapping specifically identifies the first definition.

## CellCharter

- Copyright (c) 2022, Marco Varrone. All rights reserved.
- License: BSD 3-Clause License; see [complete license text](licenses/CellCharter-LICENSE.txt).
- Upstream implementation:
  https://github.com/CSOgroup/cellcharter/blob/main/src/cellcharter/gr/_aggr.py
- DREAM location: `DREAM/DREAM_stage1/utils.py`.
- Corresponding portions: `aggregate_mean`, `aggregate_var`, `aggregate`,
  `mul_broadcast`, `setdiag`, `hop`, `normalize`, `_aggregate_neighbors`, and
  `aggregate_neighbors`.

These neighborhood-aggregation utilities are derived from CellCharter.
Differences from the inspected upstream implementation include helper-function
renaming, removal of type annotations and documentation, and simplification
of argument preprocessing in `aggregate_neighbors`.

## Provenance scope

The upstream links identify implementations reviewed on 29 October 2026, not
the exact historical commits imported into DREAM. The original import versions
and intermediate copying history are not currently recorded. These notices
cover the identified portions and do not supersede any additional applicable
copyright notices or licenses.
