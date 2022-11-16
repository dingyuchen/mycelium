---
id: ged4z9mij8tc0nr6t6ganqw
title: Elastic Search
desc: ''
updated: 1668601488707
created: 1668470853658
---

- distributed, real-time, open source, full-text search and analysis engine
- can be used for data exploration/building dashboards
- on top of apache lucene

## Querys

- RESTful APIs
- json

Interact with elasticsearch through kibana

## Logstash

data processing pipeline.

Receive data in events, processed by logstash to be shipped to elasticsearch

input sources are called _beats_


## Nodes

- master
- data
- ingest
- coordinate
  - fetch results faster
- ML

Sharding
- replica in a separate node
- zero configuration

- yellow: some nodes not set up properly
- red: big sad

# CRUD

update -> replace the whole document
update -> update only one field -> some other PUT query

POST emp/_doc/_delete_by_query
{
    ...
    {
        "_id" : "..",
    }
}

- bulk upload

- reindex
  - is a copying rather than a moving operation
  - 
  

![](2022-11-16-09-16-37.png)

standard analyzer
- lowercase, whitespace, special characters

simple 
- standard but removes numerals as well

whitespace
- split(" ")

stop
- removes words like "a", "an", "that" that are insignifcant in NLP

keyword
- exact match

fingerprint
- analyzer
- removes duplicate words