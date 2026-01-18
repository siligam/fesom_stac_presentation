---
layout: default
---

# Catalog Structure on Disk

What gets created

<div class="grid grid-cols-2 gap-4 mt-4">

<div>
  <h3 class="font-bold mb-2 text-sm">Single Collection</h3>
  
```
stac_catalog/
├── catalog.json
└── fesom-collection/
    ├── collection.json
    ├── ssh.fesom.185001.01/
    │   └── ssh.fesom.185001.01.json
    ├── ssh.fesom.185002.01/
    │   └── ssh.fesom.185002.01.json
    ├── sst.fesom.185001.01/
    │   └── sst.fesom.185001.01.json
    └── ...
```

<div class="text-xs text-gray-600 mt-2">
All items in one collection
</div>
</div>

<div>
  <h3 class="font-bold mb-2 text-sm">Per-Variable Collections</h3>
  
```
stac_catalog/
├── catalog.json
├── ssh-collection/
│   ├── collection.json
│   ├── ssh.fesom.185001.01/
│   └── ssh.fesom.185002.01/
├── sst-collection/
│   ├── collection.json
│   ├── sst.fesom.185001.01/
│   └── sst.fesom.185002.01/
└── ...
```

<div class="text-xs text-gray-600 mt-2">
Separate collection per variable
</div>
</div>

</div>
