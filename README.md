# Simple Data Infrastructure Dockerfiles

Docker Compose files for a simple data pipeline, intended for use by data engineering interview candidates.

## Problem Statement

Techncial interviews for systems candidates requires bootstrapping a lot of machinery and services.  The included `simple-data-infrastructure.yaml` adds an 'infra' target for use by Docker Compose.

## Usage

In `compose.yaml`, add:

```
include:
   - simple-data-infrastructure.yaml
...
services:
    your-service-name:
        depends_on:
        - infra
```

## Services Included:

Service                                                | Localhost | Internal
--------------------------------------------------- | ---------- | -------
Kafka-ui |       |     
Kafka (3 replicates, KRAFT, no Zookeper) | |
Postgresql | |  
Clickhouse | | 
Redis | |  
