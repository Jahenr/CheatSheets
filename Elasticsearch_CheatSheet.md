        Elasticsearch/Opensearch etc
        
        Info: Add "-u <username:password> --insecure" if the cluster uses https authentication.
        Tip: Add "?pretty" to the end of the API request to make the output more human readable.
        
        #Show cluster information
                curl -XGET https://localhost:9200/

        #Show cluster health
                curl -X GET https://localhost:9200/_cluster/health?pretty -u <username:password> --insecure

        #Show total indices
                curl -XGET https://localhost:9200/_cat/indices?pretty -u <username:password> --insecure
                or
                curl -v "localhost:9200/_cat/indices"

        #Show shards
                curl -XGET https://localhost:9200/_cat/shards?pretty -u <username:password> --insecure

        #Nodes overview
                curl -XGET http://localhost:9200/_cat/nodes?v

        #Check who is master
                curl -XGET http://localhost:9200/_cat/master?v

        #Delete an index
                curl -X DELETE 'http://localhost:9200/examples'

        #Delete status
                curl -XGET 'http://localhost:9200/_tasks?detailed=true&actions=*/delete/byquery&pretty'

        #Backup an index
                curl -XPOST --header 'Content-Type: application/json' http://localhost:9200/_reindex -d '{
                              "source": {
                              "index1": <"mainindex">
                              },
                              "dest": {
                              "index2": <"mainindex_copy">
                              }
                              }'

        #List all docs in an index
                curl -X GET 'http://localhost:9200/elasticsearch_query_examples/_search'

        #How many documents in the cluster overall
                curl -XGET http://localhost:9200/_cat/count?v

        #Shard info per index
                curl -XGET http://localhost:9200/_cat/shards/ruan-test?v

        #Shard allocation per node
                curl -XGET http://localhost:9200/_cat/allocation?v

        #Clear cache
                curl -XGET http://localhost:9200/_cache/clear

        #Create Index
                curl -XPUT http://localhost:9200/my2ndindex

        #Check pending tasks
                curl -XGET http://localhost:9200/_cat/pending_tasks?v
