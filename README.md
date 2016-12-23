# documentation

Data Model &amp; Documentation

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

* See arrows

* Always tag nodes with the channel too
* rel-types past tense
* (:User)-[:IS]->(:Person)
* (:User)-[:POSTED]->(:Content)
* (:Container)-[:CONTAINED]->(:Content)
* (:Content)-[:TAGGED]->(:Tag)-[:IS_A]->(:Concept)

## Queries

* dashboard (followship, activity)
* content discovery (projects, blogs) 
* people activity (over time, when are they falling off)
* channel activity
* identify frequent questions / topics
