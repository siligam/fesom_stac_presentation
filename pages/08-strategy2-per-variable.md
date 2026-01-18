---
layout: two-cols
layoutClass: 'grid-cols-[6fr_4fr]'
zoom: 0.9
---

# Per-Variable Collections

One collection per variable type


### Structure
- **1 Catalog** → root
- **N Collections** → one per variable
- **M Items** → files for that variable

<div class="mt-4"></div>

### Characteristics
- Variable-organized
- Direct access by variable
- No filtering needed

<div class="mt-4 p-3 bg-yellow-50 dark:bg-yellow-900 rounded text-sm">
<b>Note:</b> per experiment level catalog
</div>

::right::

<div class="ml-4">

```mermaid
graph LR
    A[fesom-catalog] --> B[ssh-collection]
    A --> C[sst-collection]
    A --> D[MLD1-collection]
    A --> E[a_ice-collection]
    A --> F[...]
    
    B --> G[ssh.fesom.185001.01]
    B --> H[ssh.fesom.185002.01]
    B --> I[ssh.fesom.185003.01]
    
    C --> J[sst.fesom.185001.01]
    C --> K[sst.fesom.185002.01]
    
    style A fill:#ffb3ba
    style B fill:#bae1ff
    style C fill:#baffc9
    style D fill:#ffffba
    style E fill:#ffdfba
    style F fill:#e0e0e0
    style G fill:#cce7ff
    style H fill:#cce7ff
    style I fill:#cce7ff
    style J fill:#d4ffd4
    style K fill:#d4ffd4
```

</div>

