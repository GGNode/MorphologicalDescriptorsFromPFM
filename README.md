# Morphological Descriptors from Phase-Field Simulations

This dataset contains morphological descriptors extracted from two-dimensional phase-field simulations of lithium dendrite growth under various operating conditions.

## Description

Each row corresponds to a simulation case defined by the following operating parameters:

- *T* — Temperature (in K)  
- *c* — Molar ratio of Li⁺ in the electrolyte (-)  
- *η*<sub>α</sub> — Activation overpotential (V)

The following morphological descriptors and instability indicators are provided:

- *T*<sub>ide</sub> — Dendrite initiation time (s): time when the first visible dendrite appears  
- *T*<sub>sc</sub> — Short-circuit time (s): time when dendrites reach 180 μm (90% of the simulation domain length)  
- *N*<sub>d</sub> — Number of dendrites: total number of distinct dendrite tips  
- *AR*<sub>max</sub> — Maximum normalized aspect ratio (unit: m·mmol⁻¹): the highest dendrite aspect ratio (height/width, dimensionless), normalized per 1 mmol/m of deposited Li  
- *AR*<sub>avg</sub> — Average normalized aspect ratio (unit: m·mmol⁻¹): the average of dendrite aspect ratios, normalized per 1 mmol/m of deposited Li  
- *τ*<sub>max</sub> — Maximum interfacial tortuosity (dimensionless): defined as  
  $$\tau = \frac{L_\text{curve}}{L_\text{straight}} \geq 1$$  
  where *L*<sub>curve</sub> is the total arc length of the dendrite front, and *L*<sub>straight</sub> is the straight-line distance across the domain.

## Handling of Missing Values

For simulation cases where dendrites did not appear before the end of simulation, *T*<sub>ide</sub> and *T*<sub>sc</sub> are not physically defined. In these cases, both values were imputed with the simulation termination time for consistency.

To assist filtering, two boolean flags are provided:

- `HasDendrite` — Whether dendrites appeared in the simulation (`True` / `False`)  
- `HasReachedHeightLimitof180μm` — Whether the dendrite tip reached 180 μm (`True` / `False`)

## Citation

Please cite the corresponding publication if you use this dataset in your research.

---
