# Memo of Understanding

**Document owner:** Pietro Moretto is responsible for developing and maintaining this document.  
**Date:** April 22, 2020  
**Version:** 1.0

## Revision History

| Version | Date     | Name            | Description      |
|---------|----------|-----------------|------------------|
| 1.0     | 22/04/2020 | Pietro Moretto | Initial document |

## 1. Purpose
The purpose of this Memorandum of Understanding (MOU) is to serve as a written understanding between ITI G. Marconi and the MarconiTT team offering services. This MOU documents the responsibilities of the principal organizations involved in the deployment of MarconiTT.

## 2. Objectives, Scope and Major Activities

### Objective
At I.T.I. G. Marconi there is a web application called MarconiTT that provides a simple and intuitive interface used to manage classroom bookings. It allows users to visualize the events and the school situations (occupied classrooms, positions of students and professors) in specific days. Also, authorized users can book classrooms or insert events. This project aims to update MarconiTT. There will be three important changes: the addition of new features that facilitate the use of the application, the encapsulation of the web application inside a containerized environment and the displacement of the entire webserver, that contains MarconiTT and other applications, from edu-x04 to edu-x08, a more modern server.

### Scope
The new features that are to be implemented will allow users to book classrooms for up to 10 hours for multiple days in consecutive weeks using the same form, as opposed to having to book for each day individually. Users will also be able to see previous bookings filtered by day thanks to a small calendar that will be implemented in the "Gestisci prenotazioni" section, as opposed to having all previous bookings in one list with no filters. The MarconiTT logo will be updated with a new one that will be created using the current I.T.I. G. Marconi logo.

The encapsulation of MarconiTT inside a containerized environment eliminates most of the difficulties that developers encounter when updating a software on production servers, since the code will reside inside an identical virtual environment on both the development and production machines.

### Major Activities
- Increase user satisfaction by allowing them to perform basic operations quicker
- Decrease the amount of time needed to update the application
- Increase overall performance
- Update the booking form so that it allows users to book the same classroom for multiple hours on multiple days of the week
- Update the *Gestisci prenotazioni* section by adding a calendar that allows users to filter previous bookings based on the selected date
- Create two containers that hold the Database and the Backend application using Docker and Docker-Compose
- Create a script that can be used to update the timetable on MarconiTT inside the containerized environment
- Move the database and the backend application inside the Docker containers
- Move the Webserver with the containerized version MarconiTT on a new server (edu-x08)

## 3. Responsibilities

### ITI G. Marconi
ITI G. Marconi is ultimately responsible for review and validation of the system documentation and proposed system modifications. In addition, ITI G. Marconi will:
1. Seek support for, program for, budget, and provide the funding necessary for successful integration of the system, including all necessary information assurance, data and computer security requirements
2. Ensure that required strategic functional plan for MarconiTT are developed
3. Provide all required information pertaining to the system, its characteristics and configuration to the MarconiTT team
4. Sign this agreement and act in the best interest of the MarconiTT team to ensure continued availability and integrity of MarconiTT and associated data

### MarconiTT team
The MarconiTT team will provide all necessary computer based services to ITI G. Marconi to ensure successfully deployment of MarconiTT. In addition, the MarconiTT team will:
1. Provide strategic guidance and oversight to ITI G.Marconi on the secure and adequate implementation of MarconiTT
2. Ensure that baseline agreements on system availability, reliability and accessibility are met or otherwise highlighted and discussed with ITI G. Marconi  
3. Define/redefine requirements and push solutions/capabilities as quickly as possible
4. Ensure support and usability 
5. Perform the necessary test operations
6. Monitor the execution of the services provided by MarconiTT, including the infrastructure efforts required ensuring continued availability

## 4. Services
- Encapsulation of the web application MarconiTT inside a containerized environment
- Displacement of the entire webserver to a more modern server
- Automatic timetable update
- Logging system
- 24/7 system availability
- Implementation of new features
- Issues report
- Testing operations
- Backup scheduled on every timetable change
- Provide support for solving bugs or explaining the functioning of the new implemented features

## 5. Duration and Amendments of the MOU

This MOU will be reviewed annually from the date signed. The ITI G. Marconi Program Manager will be responsible for this review.

## 6. Signatures
### ITI G. Marconi

**Headmaster**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
**Project Manager**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  

### MarconiTT Team

**Project Manager**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
**Developers**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
