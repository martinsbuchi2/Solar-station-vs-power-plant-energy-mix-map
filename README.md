# Solar Station vs Power Plant Energy Mix Map

**Country:** Ghana
**CRS:** EPSG:25000 - Leigon / Ghana Metre Grid
**Project file:** `Solar_Energy_Mix_Map.qgz`

---

## Overview

This project maps the geographic distribution and regional balance between conventional power plants and solar stations across Ghana. Each administrative region is characterised by its count of both asset types, enabling a regional energy mix comparison. The analysis supports renewable energy transition planning and highlights regions where solar is already the dominant generation asset type.

---

## Objectives

- Count conventional power plants and solar stations per administrative region.
- Produce a regional energy mix layer showing the ratio and count of each generation type.
- Identify regions dominated by solar assets versus those with predominantly conventional generation.

## Methodology

1. Power plants and solar stations reprojected to EPSG:25000: `power_plants_r.gpkg`, `solar_stations_r.gpkg`.
2. Administrative regions reprojected: `admin_regions_r.gpkg`.
3. Power plants spatially joined to regions; count per region stored in `plants_by_region.gpkg`.
4. Solar stations spatially joined to regions; count per region stored in `solar_by_region.gpkg`.
5. Both counts merged into a regional energy mix layer: `energy_mix_by_region.gpkg`.

## Output Layers

| File | Description |
|------|-------------|
| `power_plants_r.gpkg` | Conventional power plant locations reprojected to EPSG:25000 |
| `solar_stations_r.gpkg` | Solar station locations reprojected to EPSG:25000 |
| `admin_regions_r.gpkg` | Administrative regions reprojected to EPSG:25000 |
| `plants_by_region.gpkg` | Regions with conventional power plant count |
| `solar_by_region.gpkg` | Regions with solar station count |
| `energy_mix_by_region.gpkg` | Regions with both generation type counts and mix characterisation |

## Key Findings

- Southern regions (Western, Greater Accra, Eastern) hold the majority of conventional generation capacity, reflecting legacy investment in hydropower and thermal plants near load centres.
- Solar stations are more spatially dispersed, with a presence in regions that have no conventional power plants at all, confirming their role as the primary generation option in remote areas.
- Several northern and inland regions are solar-dominant by asset count, providing a spatial basis for prioritising battery storage and grid integration investment in those areas.

## Deliverables

| File | Type |
|------|------|
| `Solar_Energy_Mix_Map.qgz` | QGIS project |

## Notes

- No `reference_layout.png` or PDF export is present in this folder.
- All layers use EPSG:25000 (Leigon / Ghana Metre Grid).
- Asset count is a proxy for generation capacity; MW-weighted analysis would provide a more accurate picture of the actual energy mix.
