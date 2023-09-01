---
layout: splash-home
permalink: /
title: "Function-as-a-Service Package for R"
header:
  overlay_color: "#303030"
  overlay_image: /assets/images/texture.png
excerpt: "FaaSr simplifies the development of event-driven, cloud-native workflows in R"
---

{::nomarkdown}<div class="background-white"><div class="center">{:/nomarkdown}
### <i class="fas fa-cubes"></i> What is FaaSr?

FaaSr is a package that makes it easy for developers to create R functions and workflows that can run in the cloud, on-demand, based on triggers - such as timers, or repository commits. It is built for Function-as-a-Service (FaaS) cloud computing, and supports both widely-used commercial (GitHub Actions, AWS Lambda, IBM Cloud) and open-source platforms (OpenWhisk). It is also built for cloud storage, and supports the S3 standard also widely used in commercial (AWS S3), open-source (Minio) and research platforms (Open Storage Network)

With FaaSr, you can focus on developing the R functions, and leave the heavy-lifting of dealing with the idiosyncrasies of FaaS platforms to the library.

### <i class="fas fa-cubes"></i>  What can I use FaaSr for?

Originally developed to support event-driven, on-demand automated execution workflows for forecasting, FaaSr can be also useful in applications such as automated data quality assurance/control, and in general for applications where:

* You want to execute R applications in the cloud but don’t want to manage servers
* Your application is triggered by events, such as a timer or a repository push
* You want to develop your application once and be portable across multiple FaaS platforms

### <i class="fas fa-cubes"></i>  What are the pre-requisites to use FaaSr?

To use FaaSr, you need an account with a supported FaaS cloud platform (e.g. GitHub, AWS, or IBM Cloud), and an account with an S3-compliant cloud storage provider (e.g. AWS S3, Minio, or Open Storage Network)

### <i class="fas fa-cubes"></i> How do I get started?

Coming soon! The first public release of FaaSr is currently under active development with a target release in Fall'23 - please contact us if you would like to learn more about it.
