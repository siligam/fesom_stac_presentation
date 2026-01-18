---
layout: default
zoom: 0.8
---

# When to Consider Each Strategy?

Decision guide based on your use case

<div class="mt-6 p-4 bg-green-50 dark:bg-green-900 rounded">
  <h3 class="font-bold mb-2">🗂️ Consider Per-Variable Collections When:</h3>
  <div class="text-sm">
    <p class="mb-2">Typical for FESOM workflows where analysis focuses on individual variables:</p>
    <ul class="ml-4">
      <li>Variables are analyzed independently (SSH time series, SST trends, ice concentration)</li>
      <li>Performance is important for large catalogs</li>
      <li>Dataset has moderate number of variables (< 50)</li>
    </ul>
    <p class="mt-2 font-semibold">→ This aligns better with typical FESOM workflows</p>
  </div>
</div>

<div class="mt-4 p-4 bg-blue-50 dark:bg-blue-900 rounded">
  <h3 class="font-bold mb-2">📚 Consider Single Collection When:</h3>
  <div class="text-sm">
    <p class="mb-2">Better suited for multi-variable analysis:</p>
    <ul class="ml-4">
      <li>Frequently analyzing multiple variables together</li>
      <li>Users know which variable they need before querying</li>
      <li>Coupled ocean-ice analysis across variables</li>
      <li>Dataset has relatively few total items (< 1000)</li>
      <li>All variables have the same temporal coverage</li>
      <li>Simpler catalog structure is preferred</li>
    </ul>
  </div>
</div>

