---
layout: two-cols
---

# Single Collection

All variables in one collection

### Structure
- **1 Catalog** → root
- **1 Collection** → all FESOM data
- **N Items** → all NetCDF files

<div class="mt-4"></div>

### Characteristics
- Simple structure
- All data in one place
- Need to filter by variable

<div class="mt-4 p-3 bg-yellow-50 dark:bg-yellow-900 rounded text-sm">
<b>Note:</b> per experiment level catalog
</div>

::right::

<div class="ml-4">

```mermaid
graph LR
    A[fesom-catalog] --> B[fesom-collection]
    B --> C[ssh.fesom.185001.01]
    B --> D[ssh.fesom.185002.01]
    B --> E[sst.fesom.185001.01]
    B --> F[sst.fesom.185002.01]
    B --> G[MLD1.fesom.185001.01]
    B --> H[a_ice.fesom.185001.01]
    B --> I[...]
    
    style A fill:#ffb3ba
    style B fill:#4ecdc4
    style C fill:#cce7ff
    style D fill:#cce7ff
    style E fill:#d4ffd4
    style F fill:#d4ffd4
    style G fill:#ffffcc
    style H fill:#ffd4ba
    style I fill:#e0e0e0
```

</div>

