---
title: "Build Modern Python Data Pipelines with Prefect and Bauplan"
summary: "​Learn how Prefect and Bauplan work together to create a fully Python-native data platform, presented by Prefect"
tags: ["Event"]
date: 2025-12-08
showDate: true
heroStyle: "thumbAndBackground"
featurePage: true
---

[{{< icon "link" >}} Webinar Link ](https://luma.com/cf6xb4ee)

## About Event

​Python has become the language of modern data engineering, and Prefect makes orchestration in Python simple, flexible, and powerful. As data systems evolve, teams want that same simplicity for transformation and data management.

​In this webinar, we’ll show how Prefect and Bauplan work together to create a fully Python-native data platform. Prefect handles orchestration and observability. Bauplan adds a versioned, serverless lakehouse engine that brings consistency to how you build and manage data pipelines in Python.

​You’ll see:

- ​How Prefect coordinates complex pipelines across any environment.

- ​How Bauplan brings transactional, versioned data processing to Python.

- ​How to connect them for end-to-end pipelines with atomic Write-Audit-Publish flows, zero-copy branching, and detailed lineage tracking.

We’ll walk through a hands-on example using Prefect’s open-source orchestration to coordinate transformations and data publishing on Bauplan, demonstrating how to keep your stack Pythonic, transparent, and fast.

## Preface

When I first started building out data pipelines back in 2017 I was deep in the Windows environment using Task Scheduler and built-in programming logic to keep things afloat. I had done research for orchestration and came across Airflow, but it wasn't available for Windows without workarounds. A few years went by looking for a new solution when I came across a Reddit comment mentioning Prefect - this was back in 2019/2020. I remember reading how it's pure Python and knew this would a game changer. Now it's 2025 and it's amazing to see how much it's grown in popularity.

I received a Prefect Associate Certification about a year ago, but haven't had an opportunity to put it into practice. This is why I'm excited to be able to hop into this webinar - my goal is to listen and learn.

## Takeaways

What a cool experience to listen in and see how modern technologies interact with one another. Here's what I learned:

- [Bauplan](https://www.bauplanlabs.com) is a cloud-native, Python-first serverless data lakehouse platform designed to simplify data engineering by treating data pipelines, tables, and models as version-controlled software artifacts

  - The goal is to take your data from a raw stage to a gold stage
  - It handles the infrastructure layer be providing Python functions that are sent and then processed by Bauplan (functions as a service)
  - It uses Iceberg tables

- Git for Data refers to the application of version control principles, similar to those used in software development with Git, to manage data assets in data engineering, data science, and analytics workflows

- There seems to be friction in data engineering because work can't just be done in Python, but include other integrations that are not simple and create a learning curve to get started.

- Below is the GitHub repo used during the webinar:

  {{< github repo="BauplanLabs/bauplan_with_prefect" showThumbnail=false >}}

As someone who's still learning about more modern data engineering tools this was fun. Next steps for me are to do testing with the tools and build something out.
