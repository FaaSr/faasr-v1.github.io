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

These example workflows can serve as templates/starting points for your own work:

[FaaSr tutorial repository](https://github.com/FaaSr/FaaSr-tutorial) has examples for a simple 2-node sequential workflow graph for GitHub Actions, OpenWhisk, and AWS Lambda, as well as a more complex graph where execution is parallelized.

[FaaSr examples repository](https://github.com/FaaSr/FaaSr-examples) has examples in domains including ecological forecasting and biodiversity. Feel free to add pull request with other examples that have worked for you!


