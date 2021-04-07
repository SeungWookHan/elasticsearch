curl -XPUT 'http://localhost:9200/_snapshot/javacafe' -H "Content-Type: application/json" -d '{
    "type": "fs",
    "settings": {
        "location": "/tmp/es-repo/book_backup/search_example",
        "compress": true
    }
}'


curl -XGET 'http://localhost:9200/_snapshot/javacafe/_all'