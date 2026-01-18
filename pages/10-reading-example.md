---
layout: default
---

# Recap: Reading a Catalog

Both approaches appear almost identical!

<div class="grid grid-cols-2 gap-4 mt-4">

<div>
  <h3 class="font-bold mb-2 text-sm">Single Collection</h3>
  
```python
# Open catalog
catalog_path = "catalog.json"
cat = intake.open_stac_catalog(catalog_path)

# Get collection
collection = cat['fesom-collection']

# Filter for SSH files
ssh_files = []
for item_id in collection:
    if item_id.startswith('ssh.fesom.'):
        item = collection[item_id]
        asset = item._stac_obj.assets['data']
        ssh_files.append(asset.href)

# Load with xarray
ds = xr.open_mfdataset(ssh_files)
```
</div>

<div>
  <h3 class="font-bold mb-2 text-sm">Per-Variable Collections</h3>
  
```python
# Open catalog
catalog_path = "catalog.json"
cat = intake.open_stac_catalog(catalog_path)

# Get SSH collection directly
ssh_collection = cat['ssh-collection']

# Get all files (no filtering!)
ssh_files = []
for item_id in ssh_collection:

    item = ssh_collection[item_id]
    asset = item._stac_obj.assets['data']
    ssh_files.append(asset.href)

# Load with xarray
ds = xr.open_mfdataset(ssh_files)
```
</div>

</div>
