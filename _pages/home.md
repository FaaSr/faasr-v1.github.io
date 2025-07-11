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

![FaaSr logo](/assets/images/faasr_logo_white_cropped.png)

### <i class="fas fa-cubes"></i> What is FaaSr?

FaaSr is a package that makes it easy for developers to create R functions and workflows that can run in the cloud, on-demand, based on triggers - such as timers, or repository commits. It is built for Function-as-a-Service (FaaS) cloud computing, and supports both widely-used commercial (GitHub Actions, AWS Lambda, IBM Cloud) and open-source platforms (OpenWhisk). It is also built for cloud storage, and supports the S3 standard also widely used in commercial (AWS S3), open-source (Minio) and research platforms (Open Storage Network)

With FaaSr, you can focus on developing the R functions, and leave dealing with the idiosyncrasies of different FaaS platforms and their APIs to the FaaSr package.

*[<i class="fab fa-youtube" aria-hidden="true"></i> Introduction to FaaSr](
https://youtu.be/r9bHyQSUPvs)*

{% include video id="r9bHyQSUPvs" provider="youtube" %}

### <i class="fas fa-cubes"></i>  What can I use FaaSr for?

Originally developed to support event-driven, on-demand automated execution workflows for forecasting, FaaSr can be also useful in applications such as automated data quality assurance/control, and in general for applications where:

* You want to execute R applications in the cloud but don’t want to manage servers
* Your application is triggered by events, such as a timer or a repository push
* You want to develop your application once and be portable across multiple FaaS platforms

### <i class="fas fa-cubes"></i>  How do I use FaaSr?

In the typical case, to use FaaSr you:

* Develop one or more R functions 
* Complement your functions with FaaSr calls to upload/download file inputs from an S3 cloud storage
* Create a configuration for your workflow, describing the order in which your functions execute, their inputs and outputs, and credentials for the cloud computing and data services to use
* Register your workflow with your cloud computing provider
* Register triggers to start your workflow
* Access data and logs from your deployed workflows in your cloud storage provider

### <i class="fas fa-cubes"></i>  What are the pre-requisites to use FaaSr?

To use FaaSr, you need:

* A GitHub account and repository(ies) hosting your R functions
* A cloud computing account with a supported FaaS provider (e.g. GitHub Actions, AWS Lambda, and the open source OpenWhisk)
* A cloud storage account supporting S3 buckets. There are many options here, including buckets free for research use ([OSN](https://openstoragenetwork.github.io/), [NRP](https://nrp.ai)) and test/development (Minio Play), and paid-for cloud-hosted services (AWS S3)

### <i class="fas fa-cubes"></i>  I don't have yet access to S3 storage; how do I start?

* Free temporary bucket for testing: The simplest way to get started is with the free test bucket of Minio Play as per the [FaaSr tutorial](https://github.com/FaaSr/FaaSr-tutorial). This only holds data temporarily, so it is intended only for testing
* Free persistent bucket for US researchers: Sign up for an [ACCESS-CI](https://access-ci.org/) account, and request [a bucket through NRP](https://nrp.ai/documentation/userdocs/storage/ceph-s3/)
* Free persistent bucket for US researchers: If you have an [ACCESS-CI allocation](https://openstoragenetwork.github.io/docs/allocations/), you can request to [apply your ACCESS credits towards creating storage buckets](https://openstoragenetwork.github.io/docs/portal/)
* Paid persistent buckets for any users: There are several cloud providers (e.g. AWS S3) that offer S3 storage services. [This blog post](https://blog.djnavarro.net/posts/2022-03-17_using-aws-s3-in-r/) provides a nice introduction of uses of S3 in R, including how to obtain credentials for a small free tier account in AWS S3, which can be used for FaaSr.

### <i class="fas fa-cubes"></i>  In a nutshell, how does FaaSr work?

FaaSr uses Docker and cloud computing/storage APIs (Application Programming Interfaces) "under the hood" to deploy your functions: 

* Each function in your workflow runs in a Docker container in the cloud, which is deployed by your FaaS provider of choice
* The data to be used by your functions is stored persistently in a cloud S3 "bucket"
* A Docker container’s execution is "ephemeral" - i.e. no data persists after the function ends. FaaSr implements functions to download/upload data to/from a Docker container while it executes
* The FaaSr package takes care of using cloud provider specific APIs to 1) handle the passing of arguments to your function, 2) handle data transfers from/to S3 buckets, and 3) trigger the execution of “downstream” function(s) in your workflow

In other words, FaaSr deals with the specifics/complexities of multiple cloud APIs and exposes to you a simple interface that is consistent across providers.
