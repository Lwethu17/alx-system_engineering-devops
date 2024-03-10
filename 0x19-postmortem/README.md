LOAD BALANCER POSTMORTEM

DURATION
The outage occurred on March 17, 2023, from 09h00 AM to 12h09 PM (SAST) in South african time.

IMPACT
The primary service affected was our web application, resulting in complete unavailability for approximately 30% of our users during the outage period.

ROOT CAUSE
The  cause of the outage was identified as a misconfiguration in the load balancer settings, of which that leads  to an overload on one of our back-end servers.

TIMELINE:
09h00 AM: The issue was detected through monitoring alerts indicating a sudden spike in server response times.
09h07 AM: Software developers initiated an investigation right away, suspecting a potential DDoS attack due to the unusual traffic pattern.
09h35 AM: After analyzing network traffic, it was determined that the load balancer configuration might be the root cause.
10h00 AM:  Attempts were made to adjust load balancer settings, but the issue persisted.
10h58 AM: The incident was then escalated to specialist for further assistance.
11h30 AM: After extensive troubleshooting, it was confirmed that a misconfigured load balancer was causing the issue.
12h09 PM: The load balancer configuration was corrected, and normal service was restored

RESOLUTION 
Root Cause: The load balancer was misconfigured to send an excessive amount of traffic to one specific back-end server, overwhelming it’s capacity.
Resolution: The load balancer configuration was adjusted to distribute traffic evenly among all backend servers, preventing overloads and ensuring stable service.

CORRECTIVE AND PREVENTATIVE STEPS.

Improvements and fixes 

Implement automated monitoring for load balancer configurations to detect anomalies promptly.
Enhance load balancer configuration management processes to prevent misconfigurations.
Conduct regular audits of load balancer settings to identify and correct any potential issues proactively

Ways to address the issue

Update load balancer configuration to evenly distribute traffic across all backend servers.
Implement automated alerts for load balancer configuration changes.
Conduct a review of load balancer management procedures and update documentation accordingly.

