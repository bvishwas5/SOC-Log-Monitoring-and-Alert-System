# SOC Alerts

The SOC monitoring project includes five security detection alerts configured in Splunk.

## 1. Brute Force Login Detection

Detects repeated failed login attempts that may indicate a brute-force attack.

**Trigger:** Number of detection results is greater than 0.

## 2. Failed Login to Successful Login Correlation

Detects a successful authentication following failed login attempts.

**Trigger:** Per-result detection.

## 3. Privileged Account Activity Detection

Monitors authentication activity associated with the monitored test account.

**Trigger:** Detection results greater than 0.

## 4. SOC Failed Login Alert

Generates an alert when a failed login event is detected for the monitored test account.

**Trigger:** Per-result detection.

## 5. Sudden Security Event Spike Detection

Detects an unusual increase in security events compared with the normal event volume.

**Schedule:** Hourly.

**Trigger:** Detection results greater than 0.

## Alerting Workflow

Security Event → SPL Detection → Alert Trigger → SOC Dashboard → Investigation

## Alerting Platform

- Splunk Enterprise
- SPL Detection Rules
- Automated Security Alerts
- SOC Dashboard
- Windows Security Events

> All alerts were configured and tested in a controlled internship/educational environment using test security events.