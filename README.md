# splunk_docker_compose
This yaml script will deploy a small Splunk Cluster. 
One Network (SplunkNet) for Containers to communicate. 
Three SHs
One Deployer
One CM
Three IDXs
One Logstream Server

Install Docker 

https://docs.docker.com/get-docker/ 

Install Docker Compose 

https://docs.docker.com/get-started/08_using_compose/ 

Copy yaml script to your system with Docker & Docker Compose Installed 

Run Compose command:

Docker run -it -e SPLUNK_PASSWORD=<yourpassword> splunk/splunk:latest create-defaults > default.yml  

Then Run:  

SPLUNK_PASSWORD=<yourpassword> docker-compose -f ./splunkcluster.yml up -d  
