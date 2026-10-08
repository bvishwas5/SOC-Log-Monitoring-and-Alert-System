# SPL Detection Queries

This file contains the Splunk SPL queries used in the SOC Log Monitoring and Alert System project.

## 1. Brute Force Login Detection

index=* EventCode=4625
| stats count as failed_attempts by Account_Name
| where failed_attempts >= 5
| sort - failed_attempts

## 2. Failed Login to Successful Login Correlation

index=* (EventCode=4625 OR EventCode=4624)
| sort 0 _time
| streamstats count(eval(EventCode=4625)) as failed_count by Account_Name
| where EventCode=4624 AND failed_count > 0

## 3. Privileged Account Activity Detection

index=* EventCode=4624
| search Account_Name="SOC_Test_User"
| stats count by Account_Name, ComputerName

## 4. SOC Failed Login Alert

index=* EventCode=4625
| search Account_Name="SOC_Test_User"
| table _time Account_Name ComputerName EventCode

## 5. Sudden Security Event Spike Detection

index=*
| bin _time span=1h
| stats count as event_count by _time
| eventstats avg(event_count) as average_events
| where event_count > (average_events * 2)

## Tools Used

- Splunk Enterprise
- Splunk SPL
- Windows Security Event Logs
- SIEM monitoring
- Security alerting
- SOC dashboard