# Iteration Plan

**Document owner:** Pietro Moretto is responsible for developing and maintaining this document.  
**Date:** April 22, 2020   
**Version:** 1.0

## Revision History

| Version | Date     | Name            | Description      |
|---------|----------|-----------------|------------------|
| 1.0     | 22/04/2020 | Pietro Moretto | Initial document |

# 1 Iteration #1 (29/03/2019 - 04/04/2019)

## 1.1 Objectives
Encapsulate MarconiTT inside Docker containers and add new features.

## 1.2 Use Cases

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

## 1.3 Task Schedule

| Task                                           | Estimated Effort | Actual Effort | Estimated Completion Date | Actual Completion Date | Owner/s           | Status   |
|------------------------------------------------|------------------|---------------|---------------------------|------------------------|-----------------|----------|
| Learn how to use docker                        | 6                | 12            | 30/03/2019                | 31/03/2019             | Raul Farkas, Pietro Moretto, Pozzani Samuele     | Finished |
| Encapsulate MarconiTT inside Docker containers | 8                | 5             | 31/03/2019                | 31/03/2019             | Raul Farkas     | Finished |
| Add multiple days booking feature              | 7                | 7             | 02/04/2019                | 01/04/2019             | Pietro Moretto  | Finished |
| Add calendar feature and add new logo          | 8                | 8             | 04/04/2019                | 04/04/2019             | Samuele Pozzani | Finished |

# 2 Iteration #2 (14/09/2019 - 11/10/2019)

## 2.1 Objectives
Create Python scripts that allows for automatic timetable update. Move Webserver and MarconiTT on edu-x08.

## 2.2 Use Cases

### UC1 - Automatic Timetable Update

1. Log in on the pruduction server using SFTP (CLI or Filezilla)
2. Copy the updated files GPU001 and GPU004a to `/flussi_marconitt`
3. Await until the updater starts (max 60 seconds)
4. Disconnect from the production server

### UC2 - Edu-x08

1. Digit the URL `http://edu-x08/marconitt`
2. Start using the application

### UC3 - Webserver On Edu-x08

1. Digit the URL `http://edu-x08` or the alias `http://webserver`
2. Click on *AuleTT* tile
3. Now you can log in on MarconiTT using the AD credentials

## 2.3 Task Schedule

| Task                                                  | Estimated Effort | Actual Effort | Estimated Completion Date | Actual Completion Date | Owner/s                        | Status   |
|-------------------------------------------------------|------------------|---------------|---------------------------|------------------------|------------------------------|----------|
| Create Python scripts for automatic timetable updates | 20               | 20            | 08/10/2019                | 11/10/2019             | Pietro Moretto, Mateo Picari | Finished |
| Move MarconiTT on edu-x08                             | 8                | 10            | 25/09/2019                | 24/09/2019             | Raul Farkas, Samuele Pozzani | Finished |
| Move webserver with AD access API on edu-x08          | 3                | 3             | 30/09/2019                | 30/09/2019             | Raul Farkas, Samuele Pozzani | Finished |

# 3 Iteration #3 (14/10/2019 - 05/01/2020)

## 3.1 Objectives
Write software documentation. Add new API. Tweaks and bugfixes.

## 3.2 Use Cases

### UC1 - Bug fixes

1. The overall user experience has improved visually and functionally 


## 3.3 Task Schedule

| Task                         | Estimated Effort | Actual Effort | Estimated Completion Date | Actual Completion Date | Owner                                                      | Status   |
|------------------------------|------------------|---------------|---------------------------|------------------------|------------------------------------------------------------|----------|
| Write software documentation | 16               | 16            | 05/01/2020                | 05/01/2020             | Raul Farkas, Pietro Moretto, Mateo Picari, Samuele Pozzani | Finished |
| Add ETL API                  | 2                | 2             | 15/10/2019                | 15/10/2019             | Raul Farkas, Samuele Pozzani                               | Finished |
| Tweaks and bug fixes          | 15               | 18            | 20/12/2019                | 21/12/2019             | Raul Farkas, Pietro Moretto, Mateo Picari, Samuele Pozzani | Finished |

# 4 Iteration #4 (07/01/2019 - )

## 4.1 Objectives
Update software on production server. Check for minor bugs. Prepare for release

## 4.2 Use Cases

### UC1 - Product Release

1. Log in on MarconiTT using user credentials
2. You can book classrooms, view classroom bookings and events, insert events, free resources, manage classroom bookings

## 4.3 Task Schedule

| Task                                 | Estimated Effort | Actual Effort | Estimated Completion Date | Actual Completion Date | Owner                                                      | Status      |
|--------------------------------------|------------------|---------------|---------------------------|------------------------|------------------------------------------------------------|-------------|
| Update software on production server | 5                |               | 15/05/2020                |                        | Raul Farkas, Samuele Pozzani                               | Not started |
| Bug fixes / testing                  | 6                |               | 10/05/2020                |                        | Pietro Moretto, Mateo Picari                               | Started     |
| Product release                      | 3                |               | 25/05/2020                |                        | Raul Farkas, Pietro Moretto, Mateo Picari, Samuele Pozzani | Not started |