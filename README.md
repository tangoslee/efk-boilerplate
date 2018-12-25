# EFK (Elastic + Fluentd + Kibana) Boilerplate

## Structure

```bash
                                EFK Structure


        /log/{svc}/{plaform}
        e.g) /log/report/web
                              +----------------------------------------+
Server 1                      |                                        |
+---------+                +--+------+                       +---------+-+
|         |  +-----------> | 1.Nginx |                       |  5.Kibana | +----->  6.Admin
|         |                |         |                       |           |
+---------+  +-----------> +--+------+                       +---------+-+
             |                |                                        |
             |                |   +                           ^        |
             |                |   |                           |        |
+---------+  |                |   |                           +        |
|         | ++                |   v                                    |
|         |                   | 2. access.log         +-----------+    |
+---------+                   |                       |           |    |
Server n                      |       +               |           |    |
                              |       |               |           |    |
 e.g) /log/report/api         |       v               |           |    |
                              |                       |           |    |
                              |    +--------+         |           |    |
                              |    |        | +---->  |           |    |
                              |    +--------+         +-----------+    |
                              |     3.Fluentd       4.Elasticsearch    |
                              |                                        |
                              +----------------------------------------+


```

## Trace Message Format

```json
{
  "message": [string, string, string...],
  "trace": [string, string, string...],
}
```

## Operations

### Download

```bash

git clone https://github.com/tangoslee/efk-boilerplate.git

```

### Start All (Nginx + Elasticsearch + Fluentd + Kibana)

```bash

docker-compose up -d

```

### Stop All (Nginx + Elasticsearch + Fluentd + Kibana)

```bash

docker-compose down

```


