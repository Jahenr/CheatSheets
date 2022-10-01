        Elasticsearch/Opensearch etc
        
        Info: Add "-u <username:password> --insecure" if the cluster uses https authentication.
        Tip: Add "?pretty" to the end of the API request to make the output more human readable.
        
                #Show cluster information
                        curl -XGET https://localhost:9200/
                        
                #Show cluster health
                        curl -X GET https://localhost:9200/_cluster/health?pretty -u <username:password> --insecure
                        
                #Show total indices
                        curl -XGET https://localhost:9200/_cat/indices?pretty -u <username:password> --insecure
                        
                #Show shards
                        curl -XGET https://localhost:9200/_cat/shards?pretty -u <username:password> --insecure
