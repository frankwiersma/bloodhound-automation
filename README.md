# BloodHound Automation

Automatically deploy and populate a new instance of BloodHound CE on Linux systems. This tool has been tested on Ubuntu 22.04.

## How to run

```bash
usage: bloodhound-automation.py [-h] -np NEO4J-PORT -wp WEB-PORT -z ZIP [-P PASSWORD]

Automatically deploy a bloodhound instance and populate it with the SharpHound data.

optional arguments:
  -h, --help             show this help message and exit
  -np NEO4J-PORT, --neo4j-port NEO4J-PORT
                         The custom port for the neo4j container
  -wp WEB-PORT, --web-port WEB-PORT
                         The custom port for the web container (default: 8080)
  -z ZIP, --zip ZIP      The zip file from SharpHound containing the json extracts
  -P PASSWORD, --password PASSWORD
                         Custom password for the web interface (12 chars min. & must include lowercase, uppercase, digit, and special characters)
```


You can customize the Docker file located in the templates folder for further modifications.

By default, the script initializes three containers. Once the execution completes, you can shut down both the web and the PostgreSQL containers if you only want to keep the Neo4j instance running.

## Requirements
- Docker
- Docker-compose

Make sure you have both Docker and Docker-compose installed on your system for the script to work effectively.

