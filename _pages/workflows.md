---
permalink: /workflows/
title: "Workflows"
header:
  overlay_color: "#303030"
  overlay_image: /assets/images/texture.png
---

## Building your own workflows

FaaSr workflows are configured in a plain text file that follows the JSON format. Rather than edit the text file directly, the preferred method to create/edit workflows is to [use the FaaSr workflow builder Shiny app](https://faasr.shinyapps.io/faasr-json-builder/). This Shiny app allows you upload, edit, and download FaaSr-compliant configuration files without having to worry about JSON-compliant syntax and structure

## Example workflows

You can find example workflows to serve as templates or starting points for your own work. You may download the example workflows (.json files) from the repositories below to your desktop, and then upload to the [FaaSr workflow builder Shiny app](https://faasr.shinyapps.io/faasr-json-builder/) ti visualize and edit them graphically.

[FaaSr tutorial repository](https://github.com/FaaSr/FaaSr-tutorial) has examples for a simple 2-node sequential workflow graph for GitHub Actions, OpenWhisk, and AWS Lambda, as well as a more complex graph where execution is parallelized.

[neon4cast example](https://github.com/FaaSr/neon4cast-FaaSr-example) has examples for a simple single-node workflow, as well as a more complex graph where execution is parallelized, for an ecological forecasting application.

[iDigBio example](https://github.com/renatof/faasr_ridigbio_example) has an example of a simple single-node workflow for a biodiversity application.


