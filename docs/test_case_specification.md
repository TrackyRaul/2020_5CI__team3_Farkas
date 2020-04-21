# Test Case Specification

**Document owner:** Samuele Pozzani is responsible for developing and maintaining this document.  
**Date:** April 26, 2020  
**Version:** 1.0

## Table of Contents

- [Test Case Specification](#test-case-specification)
  - [Table of Contents](#table-of-contents)
  - [Revision History](#revision-history)
- [1 Introduction](#1-introduction)
- [2 Test Cases: Containers management](#2-test-cases-containers-management)
- [3 Test Cases: Timetable update](#3-test-cases-timetable-update)
- [4 Test Cases: Multiple day booking](#4-test-cases-multiple-day-booking)

## Revision History

| Version | Date     | Name            | Description      |   |
|---------|----------|-----------------|------------------|---|
| 1.0     | 04/26/20 | Samuele Pozzani | Initial document |   |
|         |          |                 |                  |   |

# 1 Introduction

This document provides the test cases to be carried out for the MarconiTT Application.<br>
Each item to be tested is represented by an individual test case. Each case details the input and expected outputs.

# 2 Test Cases: Containers management

<table>
    <tr>
        <td><b>Test ID</b></td>
        <td>2.1</td>
    </tr>
    <tr>
        <td><b>Title</b></td>
        <td>Docker startup</td>
    </tr>
    <tr>
        <td><b>Feature</b></td>
        <td>Start containers and run the application</td>
    </tr>
    <tr>
        <td><b>Objective</b></td>
        <td>Make MarconiTT accessible and usable</td>
    </tr>
    <tr>
        <td><b>Setup</b></td>
        <td>edu-x08 with running docker</td>
    </tr>
    <tr>
        <td><b>Test Data</b></td>
        <td>Root privileges are needed</td>
    </tr>
    <tr>
        <td><b>Test Actions</b></td>
        <td>Bash command input:<br>
        <code>$ docker-compose -f docker-compose-prod.yml up -d</code><br>
        (or the alias: <code>ttup</code>)</td>
    </tr>
    <tr>
        <td><b>Expected Results</b></td>
        <td>System starts the required containers and displays each output</td>
    </tr>
</table>

<br>

<table>
    <tr>
        <td><b>Test ID</b></td>
        <td>2.2</td>
    </tr>
    <tr>
        <td><b>Title</b></td>
        <td>Clean restart</td>
    </tr>
    <tr>
        <td><b>Feature</b></td>
        <td>Stop containers, clean cache and temp data, restart MarconiTT</td>
    </tr>
    <tr>
        <td><b>Objective</b></td>
        <td>Make a clean restart of MarconiTT by deleting useless data</td>
    </tr>
    <tr>
        <td><b>Setup</b></td>
        <td>edu-x08 with running docker</td>
    </tr>
    <tr>
        <td><b>Test Data</b></td>
        <td>Root privileges are needed</td>
    </tr>
    <tr>
        <td><b>Test Actions</b></td>
        <td>Bash command input:<br>
        <code>$ docker-compose -f docker-compose-prod.yml down</code><br>
        (or the alias: <code>ttdown</code>)<br>
        <code>$ docker system prune -a</code><br>
        Then restart the containers</td>
    </tr>
    <tr>
        <td><b>Expected Results</b></td>
        <td>System stops the application, deletes containers files, restarts MarconiTT</td>
    </tr>
</table>

# 3 Test Cases: Timetable update

<table>
    <tr>
        <td><b>Test ID</b></td>
        <td>3.1</td>
    </tr>
    <tr>
        <td><b>Title</b></td>
        <td>Timetable update</td>
    </tr>
    <tr>
        <td><b>Feature</b></td>
        <td>Automatically detect timetable files and update the timetable on the db</td>
    </tr>
    <tr>
        <td><b>Objective</b></td>
        <td>Simplify the timetable update process</td>
    </tr>
    <tr>
        <td><b>Setup</b></td>
        <td>edu-x08 with running docker, MarconiTT containers running</td>
    </tr>
    <tr>
        <td><b>Test Data</b></td>
        <td>Timetable files: GPU001.TXT, GPU004a.TXT</td>
    </tr>
    <tr>
        <td><b>Test Actions</b></td>
        <td>Copy timetable files into <code>/flussi_marconitt</code> on edu-x08 and wait</td>
    </tr>
    <tr>
        <td><b>Expected Results</b></td>
        <td>System automatically starts the update</td>
    </tr>
</table>

# 4 Test Cases: Multiple day booking

<table>
    <tr>
        <td><b>Test ID</b></td>
        <td>4.1</td>
    </tr>
    <tr>
        <td><b>Title</b></td>
        <td>Multiple day booking</td>
    </tr>
    <tr>
        <td><b>Feature</b></td>
        <td>Create a booking that will be repeated a specific number of weeks</td>
    </tr>
    <tr>
        <td><b>Objective</b></td>
        <td>Automatically book a room in a few clicks</td>
    </tr>
    <tr>
        <td><b>Setup</b></td>
        <td>Authorized access on MarconiTT</td>
    </tr>
    <tr>
        <td><b>Test Data</b></td>
        <td>Authorized user:<br>
        <code>Username: 17962<br>
            Password: RESERVED</code><br>
            Booking info:<br>
        <code>
            Aula: L142<br>
            Classe: 5CI<br>
            Ripetizione: 2<br>
            Giorno: 21/04/2020
            </code></td>
    </tr>
    <tr>
        <td><b>Test Actions</b></td>
        <td><ol>
            <li>Log in on MarconiTT using user credentials</li>
            <li>Select the day to create the booking</li>
            <li>Select the classroom and the repetition</li>
            <li>Select the hour</li>
            <li>Select for who is the booking</li>
            <li>Click on 'Conferma'</li></ol></td>
    </tr>
    <tr>
        <td><b>Expected Results</b></td>
        <td>MarconiTT booking confirmation</td>
    </tr>
</table>