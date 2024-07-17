---
title: Project Cauchy - Architecture
date: 2024-07-14 12:00:00 +8
categories: [Data Science]
tags: [projectcauchy]     # TAG names should always be lowercase
---

In this project, we are a fictitious gaming lab. We will evaluate hand-level data and raise any issues we find suspicious.

The high-level architecture of the company is as follows:

- `Node 1` is a FastAPI application with various endpoints. Each endpoint will provide hand-level data (i.e., the response will detail the outcome of a single hand/game). For example, the poker endpoint will provide details about a single hand of poker.

- `Node 2` will request data from `Node 1` and store it in its own production database. This database is then replicated to another database. This represents the web application we serve to our customers, along with its production and replica databases.

- MinIO is our object storage. On top of it is DuckDB, which serves as our lakehouse. We will use Delta Lake for storage. We will follow the Medallion architecture.

- Finally, a dashboard and an ML application will connect to our lakehouse.
