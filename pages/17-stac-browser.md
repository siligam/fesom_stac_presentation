---
layout: two-cols
---

# STAC Browser

Interactive web interface for exploring STAC catalogs

### Setup Steps

1. **Start STAC Browser** (port 8080)
2. **Serve catalog locally** (port 9090)
3. **Connect** browser to catalog

<div class="mt-4 p-3 bg-blue-50 dark:bg-blue-900 rounded text-sm">
 STAC Browser provides a user-friendly way to browse and visualize your STAC catalog structure
</div>

::right::

<div class="ml-4">

### 1. Clone & Run STAC Browser

```bash
git clone https://github.com/radiantearth/stac-browser.git
cd stac-browser
npm install
npm start
```

<div class="text-xs text-gray-500 mt-1">→ Opens on http://localhost:8080</div>

### 2. Serve Your Catalog

```bash
cd fesom-catalog
python -m http.server 9090
```

<div class="text-xs text-gray-500 mt-1">→ Catalog available at http://localhost:9090</div>

### 3. Connect in Browser

Enter catalog URL: `http://localhost:9090/catalog.json`

</div>
