## An ideal candidate would have:

- 1+ year of software engineering experience
    - Feel I have solid engineering experience
- Strong familiarity with PostgreSQL
    - Talk about bootcamp as well as mysql experience
- Experience with PostgreSQL disaster recovery
    - Use the PostgreSQL data base replication feature of the virtual appliance
    - Move the data base to a Network File System server
    - Schedule regular backups of the data base
- Golang
    - Google's language
    - backend language
- Experience with self-inflicted disaster recovery

## Other great skills to have:

- Kubernetes management
    - K8
    - orchestrates containerized applications to run on a cluster of hosts
    - automates deployment and management of cloud native applications using on-premises infrastructure or public cloud platforms
- Helm chart management/creation
    - Makes managing K8 clusters and containers a lot easier
    - wouldn't have to write separate YAML files for each application manually, just make a Helm chart and let Helm deploy the application to the cluster for you.
    - Contains templates for various K8 resources that combine to form an application
- Terraform experience
    - Open source infrastructure as code that allows devops engineers to programmatically provision the physical resources an application requires to run
    - Allows users to define their entire infrastructure simply by using config files and version control
- Jenkins experience
    - Jenkins is an open-source automation tool written in Java with plugins built for Continuous Integration purposes. Jenkins is used to build and test your software projects continuously making it easier for developers to integrate changes to the project, and making it easier for users to obtain a fresh build. It also allows you to continuously deliver your software by integrating with a large number of testing and deployment technologies.
- Knowledge of Groovy and Jenkinsfiles
    - 
- AWS experience, especially IAM, EC2, RDS, Route53 DNS, and VPC management
    - 
- Bash and other shell scripting
- Python
- Experience-  working around the artificial limitations of AWS RDS
- Knowledge of Docker best practices and pitfalls
- Experience with Datadog
- Experience with log aggregation and monitoring in general
- Knowledge of Security best practices and principles
- Experience with vulnerability mitigation

## Important Docker commands
After running Docker desktop

```
docker run -d nginx:latest
```

to show running containers:
```
docker ps
```

to point a port to a port in the container:
```
docker run -d -p 8080:80 nginx:latest
```

you can also do this to multiple ports
```
docker run -d -p 8080:80 -p 3000:80 nginx:latest
```

you can start containers that have been made by using start and then their name
```
docker start elastic_sanderson
```

to show all containers made:
```
docker ps -a
```

to delete a container: 
```
docker rm <name of container>
```

to delete all unused containers:
```
docker container prune
```

to name your own container
```
docker run --name  website -d -p 3000:80 nginx:latest
```

to mount a certain directory from your local environment to a container, use -v
```
docker run --name website -v $(pwd):/usr/share/nginx/html:ro -d -p 8080:80 nginx:latest
```