# Documentation

Data Model &amp; Documentation

## Steps

1. Central Neo4j Instance readonly at: bolt://all:readonly@138.197.15.1:7687, (Write-User in 1Password)
2. Develop datamodel
3. Simple Importers using Jupyter Notebooks
4. Importer Microservices as outlined below in different languages and deployment
5. Frontend Microservices for reporting / statistics / visualization / insight

## Work Split

### Will

* slack -> javascript
* twitter -> elixir
* meetup -> clojure (Mark?)

### Michael

* github -> php / js?
* stackoverflow -> python
* blogs -> Kotlin

### Ryan

* email / google group -> 


1. First get history data in
2. Store content in JSON on S3
3. dynamic import services
4. analytics


## Data Model

* [Arrows Markup](https://raw.githubusercontent.com/community-graph/documentation/master/arrows-datamodel.html)

![](community_graph.png)

* Always tag nodes with the channel too
* rel-types past tense
* (:User)-[:IS]->(:Person)
* (:User)-[:POSTED]->(:Content)
* (:Container)-[:CONTAINED]->(:Content)
* (:Content)-[:TAGGED]->(:Tag)-[:IS_A]->(:Concept)

* Minimally these properties
* (:Content {id,title, text, url, created, updated})
* (:Container {id, name, url})
* (:Tag {name})
* (:User {id, handle, name})
* (:Person {id, name})
* (:Concept {name})

## Queries

* dashboard (followship, activity)
* content discovery (projects, blogs) 
* people activity (over time, when are they falling off)
* channel activity
* identify frequent questions / topics
