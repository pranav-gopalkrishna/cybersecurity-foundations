<h1>MANAGING SECURITY RISKS</h1>

---

**Contents**:

- [Key Concepts](#key-concepts)
  - [Asset](#asset)
  - [Threat](#threat)
  - [Risk](#risk)
    - [Low-Risk Asset](#low-risk-asset)
    - [Medium-Risk Asset](#medium-risk-asset)
    - [High-Risk Asset](#high-risk-asset)
  - [Vulnerability](#vulnerability)
  - [Need for Precision in these Concepts](#need-for-precision-in-these-concepts)
- [Other Relevant Concepts](#other-relevant-concepts)
  - [Security Posture](#security-posture)
  - [Social Engineering](#social-engineering)
  - [Shared Responsibility](#shared-responsibility)
- [Further Reading](#further-reading)
- [Assignment](#assignment)

---

# Key Concepts
## Asset
An item (physical/digital/abstract) perceived as having value\*.

\* _To an organisation._

## Threat
Any circumstance/event/actor that can negatively impact assets.

---

Common threats:

- Insider threats <br> _Actors who abused authorised access_
- Advanced persistent threats <br> _Actors who keep unauthorised access for extended time-periods_

## Risk
The magnitude and likelihood of harm caused by a threat. Hence:

- Low magnitude and high likelihood may be medium-to-low risk
- High magnitude and low likelihood may be high-to-medium risk
- Low magnitude and low likelihood is low risk
- High magnitude and high likelihood is high risk

---

Hence, a risk is anything that can impact the...

- confidentiality
- integrity
- availability

... of an asset.

### Low-Risk Asset
Publicly-exposed asset that presents little-to-no risk, e.g.:

- Public website information
- Published research papers

### Medium-Risk Asset
Non-publicly-exposed asset that presents risk if exposed, e.g.:

- Quarterly earnings (could affect stock prices)
- Employee email IDs

### High-Risk Asset
Non-publicly-exposed asset protected by law/regulation, e.g.:

- Personally Identifiable Information (PII)
- Sensitive PII (SPII)
- Financial account information
- Systems access information
- Intellectual property (could give competitors unfair advantage)

## Vulnerability
A weakness that can be exploited by a threat.

---

**NOTE**: Vulnerability + Threat -> Risk

Hence, **both** must be present for there to be a risk.

## Need for Precision in these Concepts
These concepts delineate specific areas that need specific kinds of actions and action-frameworks to effectively deal with situations involving these areas. For example, a threat must be countered (either actively or using existing defenses), a risk must prepared for (e.g. by establishing protocols) and a vulnerability must be fixed (e.g. by upgrading security measures). Thus, it is key to be precise about these concepts to be precise about what action would be most effective.

# Other Relevant Concepts
## Security Posture
An organisation's ability to:

- Manage its defense of critical assets and data
- React to change

## Social Engineering
Method of exploiting of human error to gain:

- Private information
- Access
- Valuables 

## Shared Responsibility
The idea that all within an organisation take an active role in:

- Lowering risk
- Maintaining both physical and virtual security

**NOTE**: _Is a concept in security architecture and engineering._

# Further Reading
- [3 Layers of the Web](./3-layers-of-the-web.md)
- [NIST Risk Management Framework](./nist-rmf.md)
- [NIST Cybersecurity Framework](./nist-csf.md)
- [Security Control Categories](./control-categories.pdf)
- [Open Worldwide Application Security Project (OWASP)](./owasp.md)
- [Security Audit](./security-audit.md)
- [Security Information and Event Management (SIEM)](./siem.md)

# Assignment
- [Assignment](./controls-and-compliance-checklist--assignment.pdf)
- [Exemplar](./controls-and-compliance-checklist--exemplar.pdf)