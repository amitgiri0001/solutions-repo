# Dumping data from one index to another
  https://github.com/taskrabbit/elasticsearch-dump
  
  https://github.com/amitgiri0001/elasticsearch-dump


  DELETE  _*index_name*_
  
  PUT  _*index_name*_
  
  1: Add analyzer
    
    elasticdump  --input=<source_host>/<source_index>   --output=<destination_host>/<destination_index>  --type=analyzer
 
 2: Add Mapping
  
    elasticdump  --input=<source_host>/<source_index>   --output=<destination_host>/<destination_index>  --type=mapping
 3: Dump Data
    
    elasticdump  --input=<source_host>/<source_index>   --output=<destination_host>/<destination_index> --type=data
    
 3.1: Dump data with search result
  
    elasticdump  --input=<source_host>/<source_index>   --output=<destination_host>/<destination_index>   --searchBody='{ "query":{}}'
    
  3.2: Dump transformed data
     
     elasticdump  --input=<source_host>/<source_index>   --output=<destination_host>/<destination_index>  --transform='doc._source["customers"] = [ { "companyId": "ABC171", "customerNumber": "CUST001" }]'
  
