At JLab, we use containerised deployment of all the components for InevnioRDM instance. </br>
Docker Image are built manually for each release of the JRDB. These image are stored in [dockerHUB](https://hub.docker.com/repository/docker/jeffersonlab/inveniordm_jlab/general)

We plan to use GITLAB CI/CD to auto build and push docker image to dockerHUB once CI/CD becomes available.


We use two host.



- **HostA:** </br>
    Here we deploy all the services except for opensearch. The services are:</br>

    - 3 invenioRDM related containers namely web-ui, web-api and wroker. 
    - Each of redis-7, rabbitMQ-3, posgressql-12.4, nginx

- **HostB:** </br>
    Here we deploy a opensearch v2 instance.


![JLab Instance Architecture](../../docs/images/jlab-deployment-architecture.png)
