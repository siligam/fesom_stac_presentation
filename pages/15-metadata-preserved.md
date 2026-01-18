---
layout: two-cols
---

# Metadata Preserved

CF conventions and FESOM-specific attributes

**From NetCDF files:**

- CF standard names and units
- Variable descriptions
- Time coordinates
- FESOM model configuration

::right::

**In STAC items:**

```json
{
  "properties": {
    "model": "FESOM",
    "grid": "unstructured-mesh",
    "conventions": "CF-UGRID",
    "cf:parameter": [
      {
        "name": "sea_surface_elevation",
        "unit": "m"
      }
    ]
  }
}
```
