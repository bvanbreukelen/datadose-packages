# DataDose package sets

The R packages that [DataDose](https://github.com/bvanbreukelen) bundles, stored as **package sets**: one GitHub
release per set (like `packages-2026-10`), holding every file DataDose's `r-packages.lock.json` pins, and a list of
their checksums (`MD5SUMS`).

Building DataDose fetches its R packages from here, without a token, and refuses any file whose checksum differs from
its lock. So every build gets the same bytes, also when the upstream repository rebuilds a package under the same
version.

- **What the files are:** binary builds of open-source R packages from CRAN (dplyr, ggplot2, readr, …), made for
  WebAssembly by the [webR project](https://docs.r-wasm.org/) (repo.r-wasm.org). Each keeps its own licence; the
  source of each is on CRAN: `https://cran.r-project.org/package=<name>`.
- **Nothing else:** no DataDose code, courses, data or settings live here.
- **A new set** is published by DataDose's maintainers with `npm run packages -- --publish packages-YYYY-MM`.
