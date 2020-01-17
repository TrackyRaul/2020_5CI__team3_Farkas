# Project Charter

**Document owner:** Pietro Moretto is responsible for developing and maintaining this document.  
**Date:** January 05, 2020  
**Version:** 1.0

## Revision History

| Version | Date     | Name            | Description      |
|---------|----------|-----------------|------------------|
| 1.0     | 27/12/2019 | Pietro Moretto | Initial document |

## Project Title
MarconiTT 

## Start Date
29/03/2019  

## End Date
13/01/2020 

## Project Manager 
Raul Farkas 

## Project Sponsor
I.T.I. G. Marconi 

## Customer
I.T.I. G. Marconi 

## Users
I.T.I. G. Marconi teachers and school staff

## Stakeholders and Expectations  
**Team:** Implement new features, perform testing operations, report issues  
**Raul Farkas:** Call team meetings, break out tasks and assign them to teammates  
**I.T.I. G. Marconi:** Have an efficient web app to manage classroom bookings

## Purpose (Problem or opportunity addressed by the project) 
At I.T.I. G. Marconi there is a web application called MarconiTT that provides a simple and intuitive interface used to manage classroom bookings. It allows users to visualize the events and the school situations (occupied classrooms, positions of students and professors) in specific days. Also, authorized users can book classrooms or insert events. This project aims to update MarconiTT. There will be three important changes: the addition of new features that facilitate the use of the application, the encapsulation of the web application inside a containerized environment and the displacement of the entire webserver, that contains MarconiTT and other applications, from edu-x04 to edu-x08, a more modern server. 

## Goals and Objectives 
The overall objective is to add new features that increase usability and to containerize the entire application so that further developments are easier to implement on the production server.
- Increase user satisfaction by allowing them to perform basic operations quicker
- Decrease the amount of time needed to update the application
- Increase overall performance
- Update the booking form so that it allows users to book the same classroom for multiple hours on multiple days of the week
- Update the &quot;Gestisci prenotazioni&quot; section by adding a calendar that allows users to filter previous bookings based on the selected date
- Create two containers that hold the Database and the Backend application using Docker and Docker-Compose
- Create a script that can be used to update the timetable on MarconiTT inside the containerized environment
- Move the database and the backend application inside the Docker containers
- Move the Webserver with the containerized version MarconiTT on a new server (edu-x08)

## Schedule Information (Major milestones and deliverables)
- 20/03/2019 - Gather requirements
- 29/03/2019 - Iteration #1 Start (Encapsulate MarconiTT inside Docker containers and add new features)
- 04/04/2019 - Iteration #1 Complete 
- 14/09/2019 - Iteration #2 Start (Create Python scripts that allows for automatic timetable update. Move Webserver and MarconiTT on edu-x08)
- 11/10/2019 - Iteration #2 Complete 
- 14/10/2019 - Iteration #3 Start (Write software documentation. Add new API. Tweaks and bugfixes)
- 05/01/2020 - Iteration #3 Complete 
- 07/01/2020 - Iteration #4 Start (Update software on production server. Check for minor bugs. Prepare for release)
- 13/01/2020 - Iteration #4 Complete 

## Financial Information (Cost estimate and budget information) 
There will be no costs because no hardware component will be bought. Also, as this is a school project, there are no salaries. 

## Project Priorities and degrees of freedom  
The team has to respect the deadlines in order to keep up with the project and release the product. However, as this is a school project, dates can be flexible to give the team more time to analyze the obstacles encountered and learn to use new technologies. 

## Approach
Scrum methodology will be used in this project. So, an iterative and incremental approach will be adopted, with various iterations subdivided in tasks and daily team meetings to verify tasks' status and plan for new ones. 

## Constraints
In order to update the timetable on MarconiTT, an updated version of the timetable files needs to be provided. 

## Assumptions 
- A working version of MarconiTT is available and ready to be updated with new features
- The AD (Active Directory) of the school is working and can be used for authentication on MarconiTT through an API
- The server that will host the new version of MarconiTT has enough memory, disk-space and supports Docker

## Success Criteria
The web application MarconiTT needs to be fully functional inside the containerized environment on the server edu-x08. The timetable change process needs to work correctly without errors or data loss. 

## Scope
At the minimum, the web application will be incapsulated inside a containerized environment and new features will be implemented. Time permitting, the scope could be extended to include the creation of a completely automated system to update the timetable.

## Risks and obstacles to success
The team is not experienced in finishing a professional project. In fact, the team members have to work with new technologies and write the complete software documentation. Some time will be spent in debugging and fixing issues. Thus, the project end date may be delayed. 

## Signatures  
 
**Project Manager**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
**Project Sponsor**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
**Customer**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
**Technical Lead**  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
