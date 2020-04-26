# Iteration #1 Plan (29/03/2019 - 04/04/2019)

**Document owner:** Pietro Moretto is responsible for developing and maintaining this document. 
**Date:** April 22, 2020  
**Version:** 1.0

## Revision History

| Version | Date     | Name            | Description      |
|---------|----------|-----------------|------------------|
| 1.0     | 22/04/2020 | Pietro Moretto | Initial document |

## 1. Objectives
Encapsulate MarconiTT inside Docker containers and add new features.

## 2. Use Cases

### UC1 - Docker Containerization

1. Log in on the production server using SSH
2. Obtain super user privileges using:
   - `$ su`
3. Stop docker-compose:  
    - `$ docker-compose down`
4. Copy the container folder with the new changes to the docker_env folder on the server
5. Set pruduction configuration on:  
    - docker_env/angular/app/app.js
    - docker_env/node_server/config_default.js
    - docker_env/carica_orario/scripts/orario_conf.json
6. Run the following commands into the docker_env folder:
   - `$ docker system prune -a`
   - `$ docker-compose -f docker-compose-prod.yml build`
   - `$ docker-compose -f docker-compose-prod.yml up -d`
7. Disconnect from the pruduction server

### UC2 - Multiple days booking

1. Log in on MarconiTT using user credentials
2. Select the day to create the booking
3. Select the classroom and the repetition
4. Select the hour
5. Select for who is the booking
6. Click on *Conferma*
7. Disconnect from the application

### UC3 - Calendar feature

1. Log in on MarconiTT using user credentials
2. Click on *Gestisci prenotazioni*
3. Click on the calendar icon
4. Select the day
7. Disconnect from the application

## 3. Task Schedule

| Task                                           | Estimated Effort | Actual Effort | Estimated Completion Date | Actual Completion Date | Owner/s           | Status   |
|------------------------------------------------|------------------|---------------|---------------------------|------------------------|-----------------|----------|
| Learn how to use docker                        | 6                | 12            | 30/03/2019                | 31/03/2019             | Raul Farkas, Pietro Moretto, Pozzani Samuele     | Finished |
| Encapsulate MarconiTT inside Docker containers | 8                | 5             | 31/03/2019                | 31/03/2019             | Raul Farkas     | Finished |
| Add multiple days booking feature              | 7                | 7             | 02/04/2019                | 01/04/2019             | Pietro Moretto  | Finished |
| Add calendar feature and add new logo          | 8                | 8             | 04/04/2019                | 04/04/2019             | Samuele Pozzani | Finished |
