---
layout: two-cols
zoom: 0.9
---

# STAC Hierarchy

The three core components

### 📚 Catalog
  - Top-level container
  - Groups related collections
  - Entry point for discovery

<div class="mt-4"></div>

### 📂 Collection
  - Group of related items
  - Shared metadata (extent, license)
  - Describes what's inside

<div class="mt-4"></div>

### 📄 Item
  - Individual asset (e.g., NetCDF file)
  - Specific time & space
  - Links to actual data

::right::

<div class="ml-4">

```mermaid
graph TD
    A[Catalog] --> B[Collection 1]
    A --> C[Collection 2]
    A --> D[Collection 3]
    B --> E[Item 1]
    B --> F[Item 2]
    C --> G[Item 3]
    C --> H[Item 4]
    D --> I[Item 5]
    
    style A fill:#ff6b6b
    style B fill:#4ecdc4
    style C fill:#4ecdc4
    style D fill:#4ecdc4
    style E fill:#95e1d3
    style F fill:#95e1d3
    style G fill:#95e1d3
    style H fill:#95e1d3
    style I fill:#95e1d3
```

</div>
