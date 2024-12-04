elasticSearch is search engine

-> used for searching, analyzing, and visualizing large volumes of structured or unstructured data in real time

->achieve fast search responses because instead of searching the text directly, it search index

*Stores data as JSON documents

=>inverted index because it inverts page centric data structure (page->words) to keyword centric data structure (words->page)

**componnents of elasticSearch :

index : one or more documents

document : one or more fields

shards : Data is stored in indices (similar to databases), which are divided into shards which contains multiple documents

Replica : copy of index

***Inverted index :  Instead of mapping rows to values, it maps terms (words) to the documents in which they appear.

Term      | Documents
-----------|-----------
the       | Doc 1, Doc 2
quick     | Doc 1

****flow architecture : query->api->index (which contains multiple shards) : request will go to shards concurrently

response come with details (what shard contains value and what's the total) and time took to search

*****elastic search configuration :

-we need to specify cluster name and path data where to store our indexes (storage) in elasticsearch.yml Under config document

-run elasticSearch.bat Under bin
