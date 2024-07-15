---
title: Project Cauchy - Architecture
date: 2024-07-14 12:00:00 +8
categories: [Data Science]
tags: [projectcauchy]     # TAG names should always be lowercase
---

In this project, we are a fictitous Online Casino Company.

The high level architecture of the company is as follows

- `node 1` is a FastAPI application that has various endpoints. Each endpoint will spitout hand-level data (i.e. the response will give you the outcome of a single hand/game). For example, the poker endpoint will give you details about a single hand of poker. This represents various third party provider of games.

- `node 2` will request from `node 1` and store it on its own production database. This database is then replicated to another database.  This represents a web application that we are serving to our customer, alongside its production DB and it's replica DB.

- `MinIO` is our object storage. On top of it is `DuckDB`. It will serve as our lakehouse. (We will be using Delta Lake for our storage.) We will follow Medallion architecture.

- Finally, a dashboard and an oML application will be connected to our lakehouse.

![alt text](/assets/images/post_0003/arch.png "architecture")
