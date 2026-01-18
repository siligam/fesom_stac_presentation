---
layout: default
zoom: 0.8
---

# Reading Per-Variable Collections

Direct access to variable collections

```python {all|4-5|8-10|13|17-18|all}
import intake
import xarray as xr

catalog_path = "/path/to/catalog.json"
cat = intake.open_stac_catalog(catalog_path)

# See available collections
print("Available variables:")
for collection_id in cat:
    print(f"  - {collection_id}")

# Direct access to SSH collection - no filtering!
ssh_collection = cat['ssh-collection']

# Get all files from this collection
ssh_files = []
for item_id in ssh_collection:
    item_source = ssh_collection[item_id]
    stac_item = item_source._stac_obj
    asset = stac_item.assets['data']
    ssh_files.append(asset.href)

# Load with xarray
ds = xr.open_mfdataset(ssh_files, combine='by_coords')
```


<div v-click class="mt-4 p-3 bg-green-50 dark:bg-green-900 rounded text-sm">
✅ <b>Benefit:</b> No filtering logic needed - direct variable access
</div>
