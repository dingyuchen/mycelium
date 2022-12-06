---
id: qffz5o5bj5gygqmpo4kz9vo
title: Kibana
desc: ''
updated: 1670335019623
created: 1669163020252
---

# Sidebar

## Analytics

### Discover

- playground to write queries

### Dashboard

- visualize some data

### Canvas

- create presentations

### Maps

- visualization for geographical data

### Machine Learning

## Observability

## 

- saving queries,
- KQL
- saving search (csv)
- inspect kql query as DSL
- 

## Spaces

- Anything that is saved, is called a save object

## Logstash

> Needs installation separate from kibana and elasticsearch

```
// logstash/config/sample.conf
input {
    stdin {
        codec => json
    }
    http {
        host => "localhost" # http plugin
        port => "8080"
    }
}

output {
    stdout {}
    file {
        path => "output.txt"
    }
}
```

> ./bin/logstash -f config/sample.conf



```
filter {
    mutate {
        # add or remove fields
    }
    grok {
        match => {
            "message" => ""
        }
    }
}
```

grok patterns are like regex but with labeling


