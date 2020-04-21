# System Documentation

**Document owner:** Raul Farkas is responsible for developing and maintaining this document. 
**Date:** April 21, 2020  
**Version:** 1.0

## Revision History

| Version | Date       | Name        | Description      |
| ------- | ---------- | ----------- | ---------------- |
| 1.0     | 21/04/2020 | Raul Farkas | Initial document |

## Introduction

MarconiTT is a web application available to desktop and mobile users and accessible through a browser. It can be reached both from inside and outside the school network. The application allows for authorized teachers, students and staff members to book school classrooms and labs. This document will provide instructions on how to install the system requirements, a fresh copy of MarconiTT, how to do the initial configuration and add the initial timetable and how to change the timetable.

## Processes

### System requirements installation

Before cloning the MarconiTT repository on the server, it is required to install Docker, docker-compose, apache, git. The installation of Apache webserver and git is simple and intuitive, so this part of the documentation will focus only on the installation of Docker and docker-compose.

#### Steps

Keep in mind that by installing docker-compose you also install Docker.

1. Start by downloading the Docker Compose binary into the `/usr/local/bin` directory using the following [`curl`](https://linuxize.com/post/curl-command-examples/) command:

   ```bash
   $ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
   ```

2. When the download is complete, give [executable permissions](https://linuxize.com/post/chmod-command-in-linux/) to the Compose binary:

   ```bash
   $ sudo chmod +x /usr/local/bin/docker-compose
   ```

3. Verify the installation by typing:

   ```bash
   $ docker-compose --version
   #OUTPUT:
   #docker-compose version 1.23.1, build b02f1306
   ```

### MarconiTT installation

#### Steps

1. Clone the repository https://github.com/TrackyRaul/MarconiTT.git in a chosen directory on the server.

2. Checkout to the "mod_for_prod" where the production version of MarconiTT can be found.

   ```
   $ git checkout mod_for_prod
   ```

3. Configure frontend application. Open the frontend configuration  that can be found in "docker_env\angular\app\app.js".

   ```javascript
   app.constant("CONFIG", {
       'HOST' : 'edu-x08',
       'PORT': '8090'
   });
   ```

   The HOST attribute should be configured to point to the node.js Express backend which can be found inside the docker containers. The PORT should remain 8090.

4. Copy the angular frontend application inside the publishing directory of your webserver. If you are using Apache that directory is "/var/www/html/". Make sure you configure the virtual hosts appropriately based on your webserver configuration and structure.

5. Configure backend application. Open the backend configuration that can be found in "C:\Users\raulf\Desktop\Projects\x documentazione tt\MarconiTT\docker_env\node_server\config_default.js".

   The "webserver" attribute should point to the webserver where the LDAP login script is located.

   Do not change in any way the fields regarding the DB configuration.

6. Initial configuration of the DB through the updater container and script. Open the Updater configuration file that can be found in "docker_env\carica_orario\scripts\orario_conf.json\"

   Make sure that the "first_time" attribute is set to 1 and that the "files_to_check" are set to ["GPU001.txt", "GPU004a.txt"].

7. Provide the json files containing "aule" information. This can be simply done by adding the "aule.json" file in "docker_env\carica_orario\scripts\aule.json"

   The "aule.json" file should look like this.

   ```json
   {"classes":["1AI","1BI"....]}
   ```

8. Provide the csv files containing "vacanze" and "periodo" information. This can be done by adding the "vacanze.csv" and the "periodo.csv" files in the "docker_env\carica_orario\scripts\" directory.
9. Provide "flussi" files. This can be done by adding the "GPU001.txt" and  "GPU004a.txt" files in "docker_env\carica_orario\scripts\flussi"

