---
permalink: /install/
title: "Installing FaaSr"
header:
  overlay_color: "#303030"
  overlay_image: /assets/images/texture.png
---

# Install stable release from CRAN

Coming soon!

## Install development release from GitHub

```
devtools::install_github('FaaSr/FaaSr-package',force=TRUE)
library('FaaSr')
```
## Dependences

The main dependences are listed in the [FaaSr package description](https://github.com/FaaSr/FaaSr-package/blob/main/DESCRIPTION)

While not a dependence, it is also highly recommended that you install the [minioclient](https://cran.r-project.org/web/packages/minioclient/index.html) to browse S3 contents directly from your Rstudio session
