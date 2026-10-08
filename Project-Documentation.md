\# Project Documentation



\## Project Title



SOC Log Monitoring and Alert System



\## Project Purpose



The purpose of this project is to demonstrate a basic Security Operations Center (SOC) monitoring workflow using Splunk. Security events are collected and analyzed to identify suspicious authentication activity and generate alerts.



\## Problem Statement



Organizations generate large numbers of security events from systems and applications. Without centralized monitoring, suspicious activities such as repeated failed logins can be difficult to identify.



This project uses Splunk as a SIEM platform to centralize security event monitoring, apply detection logic, generate alerts, and provide dashboard-based visibility.



\## Architecture



Security Events

&#x20;       ↓

Windows Security Logs

&#x20;       ↓

Splunk Enterprise

&#x20;       ↓

SPL Detection Rules

&#x20;       ↓

Security Alerts

&#x20;       ↓

SOC Dashboard

&#x20;       ↓

Investigation



\## Implemented Detection Use Cases



\### 1. Brute Force Login Detection



Identifies repeated failed authentication attempts that may indicate a brute-force attack.



\### 2. Failed Login to Successful Login Correlation



Identifies successful authentication occurring after failed authentication attempts.



\### 3. Privileged Account Activity Detection



Monitors authentication activity associated with the monitored test account.



\### 4. SOC Failed Login Alert



Generates an alert when failed authentication activity is detected.



\### 5. Sudden Security Event Spike Detection



Identifies unusual increases in security event volume.



\## Alerting



Five detection alerts were configured in Splunk:



\- Brute Force Login Detection

\- Failed Login to Successful Login Correlation

\- Privileged Account Activity Detection

\- SOC Failed Login Alert

\- Sudden Security Event Spike Detection



\## Dashboard



A Splunk SOC dashboard was created to provide visual visibility into security events and suspicious login activity.



Screenshots of the dashboard and detection results are included in the Screenshots directory.



\## Technologies Used



\- Splunk Enterprise

\- SPL

\- Windows Security Event Logs

\- SIEM

\- Security Monitoring

\- Security Alerting

\- Dashboard Visualization



\## Skills Demonstrated



\- Log analysis

\- SIEM monitoring

\- SPL query writing

\- Security detection

\- Alert configuration

\- Dashboard creation

\- Basic incident investigation

\- SOC workflow understanding



\## Project Outcome



The project demonstrates an end-to-end beginner SOC monitoring workflow from security event analysis to detection, alert generation, dashboard monitoring, and investigation.



\## Environment



The project was developed and tested using controlled security events in an educational/internship environment.



\## Disclaimer



No real organizational security data or credentials are included in this repository.

