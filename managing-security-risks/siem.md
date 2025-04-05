<h1>SIEM</h1>

**_Security Information and Event Management_**

---

**Contents**:

- [Concepts](#concepts)
  - [Log](#log)
    - [Definition](#definition)
    - [3 common log sources:](#3-common-log-sources)
    - [Importance of understanding logs](#importance-of-understanding-logs)
  - [SIEM](#siem)
    - [Definition](#definition-1)
    - [Usefulness](#usefulness)
    - [SIEM tools increase efficiency in security operation](#siem-tools-increase-efficiency-in-security-operation)
    - [Customising SIEM tools](#customising-siem-tools)
  - [Dashboard](#dashboard)
- [SIEM dashboard](#siem-dashboard)
  - [Creation](#creation)
  - [Purpose](#purpose)
    - [Overview](#overview)
    - [Provide comprehensive summary of security-related data](#provide-comprehensive-summary-of-security-related-data)
    - [Provide stakeholders with different metrics](#provide-stakeholders-with-different-metrics)
- [Exploring SIEM tools](#exploring-siem-tools)
  - [Types](#types)
  - [Common tools](#common-tools)
  - [Open-source vs. proprietary tools](#open-source-vs-proprietary-tools)
    - [Open-source](#open-source)
    - [Proprietary](#proprietary)
- [SOAR: Automation in the use of SIEM tools](#soar-automation-in-the-use-of-siem-tools)

---

# Concepts
## Log
### Definition
Record of events in an organisation's systems and/or networks.

### 3 common log sources:

- Firewall logs; record of:
    - Attempted or established connections <br> _For incoming traffic from the internet_
    - Outbound requests from within the network <br> _To the internet_
- Network logs; record of:
    -  Computers and devices entering/leaving network
    -  Connections between devices and services on network.
- Server logs; record of:
    - Events related to services <br> _E.g. websites, emails, file shares, etc._
    - Authorisation and access-related actions <br> _E.g. login, password, username requests, etc._

### Importance of understanding logs
By monitoring logs, security teams can identify:

- Vulnerabilities
- Potential data breaches

Crucially, **_SIEM tools rely on logs to_**:

- Monitor systems
- Detect security threats

## SIEM
### Definition
_Security Information and Event Management_

An application that...

- collects
- analyses

... **_log data to monitor critical activities_** in an organisation.

### Usefulness
- Provides real-time information visibility
- Provides event monitoring and analysis
    - Threats
    - Risks
    - Vulnerabilities
- Provides automated alerts
- Stores all log data in a centralised location

### SIEM tools increase efficiency in security operation
SIEM tools index and minimise the number of logs to review

=> They increase efficiency in detection and analysis

### Customising SIEM tools
SIEM tools must meet an organisation's unique security needs

=> It must be accordingly configured and customised

---

New threats and vulnerabilities need to be detected and addressed

=> SIEM tool customisation is continual

## Dashboard
- A structured visual interface displaying metrics and data
- Designed for real-time monitoring, analysis and decision-making

# SIEM dashboard
## Creation
SIEM tools can be used to create dashboards.

## Purpose
### Overview
1. Provide a comprehensive summary of security-related data
2. Provide stakeholders with different metrics

---

**DEFINITION: Metrics**:

Key technical attributes used to assess software performance.

E.g.:

- Response time
- Availability
- Failure rate

### Provide comprehensive summary of security-related data
**Dashboards (_in general_)**:

Help people make quick and informed decisions based on data.

**SIEM dashboards**:

- Help _security analysts_ easily access security information
- For convenience, the information is accessed in the form of:
    - Charts
    - Graphs
    - Tables

**NOTE**: _Visualisation can aid in information comprehension._

---

**E.g.: Alert about a suspicious login attempt**:

- The analyst accesses their SIEM dashboard
- Gathers information about this alert
- INFO: 500 login attempts for an employee's account in 5 minutes
- INFO: Login attempts happened:
    - From locations outside of their usual location
    - In times outside of their usual working hours

Thus, using a dashboard, the security analyst is able to review:

- Visual representations of the timeline of the login attempts
- Location and exact time of the activity

With this, they can determine that the activity was suspicious.

### Provide stakeholders with different metrics
SIEM dashboards can be customised to display...

- specific metrics
- other data

... that are relevant to different members in an organisation.

---

E.g.: Display metrics for monitoring everyday business operations:

- Volume of incoming and outgoing network traffic
- Number of failed authorisation attempts

This would be relevant for a security analyst.

# Exploring SIEM tools
## Types
- Self-hosted
    - Install, operate, maintain using own physical infrastructure
    - Managed and maintained by organisation's IT department
- Cloud-hosted
    - SIEM tool services accessible via internet
    - Managed and maintained by SIEM providers (3rd party)
- Hybrid
    - Has self-hosted and cloud-hosted components
    - Allows effective division of infrastructure, e.g.:
        - Own physical infrastructure for confidential data
        - Cloud infrastructure for lower risk data

## Common tools
- Splunk Entreprise (self-hosted)
- Splunk Cloud (cloud-hosted)
- Google Chronicle (cloud hosted)

## Open-source vs. proprietary tools
### Open-source
- Public exposure and immediate access to the source code
- Free to use, improve and _customise_
- Allows quick identification and rectification of issues <br> _This often makes security issues less likely to occur_
- Encourages wider collaboration

### Proprietary
- Only owners can access and modify the source code
- Identified issues must be fixed via updates by owners

# SOAR: Automation in the use of SIEM tools
**CHALLENGE**:

The more interconnected devices there are, the larger the cybersecurity attack surface and the amount of data that threat actors can exploit. The diversity of attacks and data that require special attention is expected to grow significantly.

---

**POTENTIAL OF AUTOMATION**:

The implementation of automation will help security teams respond faster to possible incidents, performing many actions without waiting for a human response. **Security orchestration, automation, and response (SOAR)** is a collection of applications, tools, and workflows that uses automation to respond to security events. Essentially, this means that handling common security-related incidents with the use of SIEM tools is expected to become a more streamlined process requiring less manual intervention.

This frees up security analysts to handle more complex and uncommon incidents that, consequently, cannot be automated with a SOAR. Nevertheless, the expectation is for cybersecurity-related platforms to communicate and interact with one another. Although the technology allowing interconnected systems and devices to communicate with each other exists, it is still a work in progress.