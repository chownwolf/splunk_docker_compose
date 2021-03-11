# splunk_docker_compose
This yaml script will deploy a small Splunk Cluster. 
One Network (SplunkNet) for Containers to communicate. 
One SH
One CM
Three IDXs
One HF
One Logstream Server

Install Docker 

https://docs.docker.com/get-docker/ 

Install Docker Compose 

https://docs.docker.com/get-started/08_using_compose/ 

Copy yaml script to dev system 

https://visicore.sharepoint.com/Shared%20Documents/Forms/AllItems.aspx?viewpath=%2FShared%20Documents%2FForms%2FAllItems%2Easpx&newTargetListUrl=%2FShared%20Documents&viewid=74f7f91a%2Dd508%2D4a8f%2D9e85%2D7ea81ae9d045&id=%2FShared%20Documents%2FDocker%5FSplunk 

Run Compose command 

Docker run -it -e SPLUNK_PASSWORD=<yourpassword> splunk/splunk:latest create-defaults > default.yml  

This creates the shared password for cluster 

SPLUNK_PASSWORD=<yourpassword> docker-compose -f ./splunkcluster.yml up -d  
