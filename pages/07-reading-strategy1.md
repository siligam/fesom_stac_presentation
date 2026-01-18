---
layout: default
zoom: 0.9
---

# Reading Single Collection

Using intake-stac with filtering

```python  {all|4-5|8|13|all}
import intake
import xarray as xr

catalog_path = "/path/to/catalog.json"
cat = intake.open_stac_catalog(catalog_path)

# Access the single collection
collection = cat['fesom-collection']

# Filter items by variable name
ssh_files = []
for item_id in collection:
    if item_id.startswith('ssh.fesom.'):
        item_source = collection[item_id]
        stac_item = item_source._stac_obj
        asset = stac_item.assets['data']
        ssh_files.append(asset.href)

# Load with xarray
ds = xr.open_mfdataset(ssh_files, combine='by_coords')
```


<div v-click class="mt-4 p-3 bg-yellow-50 dark:bg-yellow-900 rounded text-sm">
⚠️ <b>Note:</b> Requires filtering logic to select specific variables
</div>
