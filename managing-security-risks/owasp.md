<h1>OWASP</h1>

**OWASP =**

- **Open Web Application Security Project (previous name)**
- **Open Worldwide Application Security Project (current name)**

---

**Contents**:

- [Concepts](#concepts)
  - [Attack Surface Area](#attack-surface-area)
  - [Attack Vector](#attack-vector)
- [Principles](#principles)
  - [1. Minimise Attack Surface Area](#1-minimise-attack-surface-area)
    - [Key Sub-Principle: Principle of Least Privilege](#key-sub-principle-principle-of-least-privilege)
  - [2. Defence in Depth](#2-defence-in-depth)
  - [3. Separation of Duties](#3-separation-of-duties)
  - [4. Keep Security Simple](#4-keep-security-simple)
  - [5. Fix Security Issues Correctly](#5-fix-security-issues-correctly)
  - [6. Establish Secure Defaults](#6-establish-secure-defaults)
  - [7. Fail Securely](#7-fail-securely)
  - [8. Do Not Trust Services](#8-do-not-trust-services)
  - [9. Avoid Security by Obscurity](#9-avoid-security-by-obscurity)

---

# Concepts
## Attack Surface Area
All potential vulnerabilities a threat actor could exploit, e.g.:

- Attack vectors
- Networks using outdated protocols
- Human error
- Software features, such as:
    - Verbose logging (that could expose sensitive information)
    - Debug mode enabled in production <br> _Exposes internal system functionality to attackers_
    - Unrestricted file execution
    - Insecure API endpoints

## Attack Vector
A pathway an attacker can use to penetrate security defenses, e.g.:

- Weak password
- Phishing email

# Principles
Use these security principles to...

... _promote safe development practices_

... that _reduce risks_ to _companies and users_ alike.

## 1. Minimise Attack Surface Area
Minimise attack surface by managing risk.

---

### Key Sub-Principle: Principle of Least Privilege
Users have the least amount of access needed for their purposes.

- Limits excessive/unnecessary access to assets and information
- Reduces the amount of damage a security breach could cause

## 2. Defence in Depth
There must be multiple security controls...

... addressing risks and threats in different ways.

---

E.g.:
- Multi-factor authentication (MFA) <br> _Additional security controls added to password_
- Security permissions <br> _Additional restrictions added to organisation credentials_
- Firewalls <br> _Additional restrictions added to network access controls_

## 3. Separation of Duties
Limit access privilege by delimiting duties assigned to users.

MOTIVATION: _No one should be given too many privileges._

---

E.g.:

- Person signing paychecks != Person preparing paychecks
- Developer deploying code != Engineer approving deployment

---

**NOTE**: Related to separation of concerns in software.

## 4. Keep Security Simple
**Conceptual Setup**:

1. Focus is finite, demanding prioritisation and efficiency
2. Thus, reality must be dealt with via a _few_ mental units
3. The same applies for security, which is a part of reality

---

**Principle Statement**:

Ensure that any aspect of security can be simplified:

- Conceptually:
    - Reduce framework to functional units
    - Reduce relationships to interactions and constraints
- Technically:
    - Reduce requirements to procedures and tasks
    - Reduce automation to modules

---

**Additional Points**:

- Complicated solutions can become unmanageable
- Complexity in security controls => Difficulty in collaboration
- In short, complexity makes security difficult

## 5. Fix Security Issues Correctly
Identify root causes of issues quickly and accurately, i.e.:

- Categorise (e.g. via [security domain](../foundations-of-cybersecurity/8-cybersecurity-domains.md))
- Identify threat/risk level
- Identify threatened/at-risk assets/information
- Identify vulnerabilities that are/can be exploited
- Conduct tests to ensure fixes are successful

## 6. Establish Secure Defaults
Optimal security state = Default state for users

_It should take extra work to make the application insecure._ 

## 7. Fail Securely
If a control fails or stops, default to the most secure option.

---

E.g. Firewall failure =>

- Close all connections
- Block all new connections

... _NOT start accepting everything._

## 8. Do Not Trust Services
Do not explicitly and automatically trust 3rd-party systems.

_3rd-party systems may have different security policies._

---

E.g.: Consider the following case:

- 3rd-party vendor tracks reward points for airline customers
- Airline wants to use this information to fix customer balance

Airline must ensure reward information is accurate before using it.

## 9. Avoid Security by Obscurity
**Conceptual Setup**:

Any hidden security-related detail is a vulnerability.

_Why? Because its breach is a direct security threat._

---

**Principle Statement**:

Hence, do not rely on hiding details to maintain security.

_Design systems assuming attackers have knowledge of details._

---

E.g.: The security of an software/web application

- Should not rely on keeping the source code secret
- Should rely on many other factors:
    - Reasonable password policies
    - Defense in depth
    - Business transaction limits
    - Solid network architecture
    - Fraud and audit controls