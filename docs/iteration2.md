# Iteration #2 Plan (14/09/2019 - 11/10/2019)

**Document owner:** Pietro Moretto is responsible for developing and maintaining this document. 
**Date:** April 22, 2020  
**Version:** 1.0

## Revision History

| Version | Date     | Name            | Description      |
|---------|----------|-----------------|------------------|
| 1.0     | 22/04/2020 | Pietro Moretto | Initial document |

## 1. Objectives
Create Python scripts that allows for automatic timetable update. Move Webserver and MarconiTT on edu-x08.

## 2. Use Cases

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

## 3. Task Schedule

| Task                                                  | Estimated Effort | Actual Effort | Estimated Completion Date | Actual Completion Date | Owner/s                        | Status   |
|-------------------------------------------------------|------------------|---------------|---------------------------|------------------------|------------------------------|----------|
| Create Python scripts for automatic timetable updates | 20               | 20            | 08/10/2019                | 11/10/2019             | Pietro Moretto, Mateo Picari | Finished |
| Move MarconiTT on edu-x08                             | 8                | 10            | 25/09/2019                | 24/09/2019             | Raul Farkas, Samuele Pozzani | Finished |
| Move webserver with AD access API on edu-x08          | 3                | 3             | 30/09/2019                | 30/09/2019             | Raul Farkas, Samuele Pozzani | Finished |
