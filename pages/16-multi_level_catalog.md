---
layout: default
---

# Multi-level Catalog (strategy 2: per-variable)

Organizing experiments hierarchically

<div class="grid grid-cols-2 gap-8 mt-6">

<div>

### 📋 Key Concepts

<div class="mt-4 space-y-3">

<div class="p-3 bg-blue-50 dark:bg-blue-900 rounded">
  <div class="font-semibold text-sm">📚 Catalogs can nest</div>
  <div class="text-xs text-gray-600 dark:text-gray-300 mt-1">A catalog can contain other catalogs</div>
</div>

<div class="p-3 bg-orange-50 dark:bg-orange-900 rounded">
  <div class="font-semibold text-sm">📂 Collections are terminal</div>
  <div class="text-xs text-gray-600 dark:text-gray-300 mt-1">A collection cannot contain other collections</div>
</div>

</div>

### 🏗️ General Structure

```
📚 Catalog (root)
└── 📚 Catalog (experiment 1)
    └── 📂 Collection (variable)
        └── 📄 Item(s)
└── 📚 Catalog (experiment 2)
    └── 📂 Collection (variable)
        └── 📄 Item(s)
```

</div>

<div>

### 🌊 FESOM Example

<div class="mt-4">

```
📚 root-catalog
└── 📚 awiesm-basic-001
    ├── 📂 mld
    │   └── Collection (MLD1)
    │       └── 📄 Item(s)
    └── 📂 temp
        └── Collection (TEMP)
            └── 📄 Item(s)
```

</div>

<div class="mt-6 p-4 bg-green-50 dark:bg-green-900 rounded text-sm">
  <div class="font-bold mb-2">✨ Benefits</div>
  <ul class="text-xs space-y-1 ml-4">
    <li>Organize by experiment/simulation</li>
    <li>Logical grouping of related data</li>
    <li>Easy to navigate and discover</li>
    <li>Scalable for multiple experiments</li>
  </ul>
</div>

</div>

</div>