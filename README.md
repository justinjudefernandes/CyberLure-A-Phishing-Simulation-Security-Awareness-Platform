# 🛡️ CyberLure: A Phishing Simulation & Security Awareness Platform
> ##### (Mandatory Training · Phishing Awareness · Phishing Campaigns · IT Training · Gamification)


## 🎯 Objective:
Security awareness is most effective when organizations can continuously educate, test, measure, and remediate employee behaviour. The objective of CyberLure was to build a complete security-awareness lifecycle rather than a standalone phishing simulator:

              Train → Simulate → Measure → Remediate → Verify → Re-measure

The platform enables security teams to:
- Deliver mandatory organizational training
- Educate employees about current cyber threats
- Run controlled phishing simulations
- Measure individual and organizational behaviour
- Automatically assign remedial training
- Verify training completion and assessment performance
- Reinforce learning through security games
- Generate certificates and compliance reports
- Measure human cyber risk through behavioural analytics

The platform was designed to operate without relying on external SaaS platforms or continuous internet connectivity.

## 🧰 Technology Stack:
| Layer | Technology |
|---|---|
| **Frontend** | Jinja2 · vanilla JavaScript · inline SVG |
| **Backend** | Python · Flask · SQLAlchemy |
| **Database** | SQLite (zero-dependency default) · PostgreSQL/MySQL-ready |
| **Auth & Directory** | Session auth + role-based access control · LDAP/Active Directory (ldap3) |
| **Email** | SMTP delivery · open/click tracking pixels & per-recipient tokens |
| **Certificates** | Headless Chromium → PDF generation |
| **AI (optional)** | Anthropic Claude API for content assistance, with a deterministic offline fallback |
| **Deployment** | Runs on a single host · **offline / air-gapped mode** for regulated networks |

## 📊 Platform Overview:

CyberLure combines five major capabilities into one security-awareness platform:<br>
1) 🎓 **Mandatory Training**<br>
2) 🛡️ **Phishing Awareness**<br>
3) 🎣 **Phishing Campaigns**<br>
4) 🖥️ **IT Training**<br>
5) 🎮 **Gamification**

These capabilities are supported by organization-wide dashboards, executive and detailed reporting, user management, role-based access control, and integrations such as SMTP, LDAP/Active Directory, and NTP.

> 🤖 **AI-Assisted Content Development:** <br>
AI tools were used as development and content-assistance tools throughout the project to accelerate the creation of training and security-awareness content. After reviewing the relevant training materials, Claude was used to generate initial drafts of assessment questions, quizzes, learning content, and related materials based on the learning objectives and subject matter. All generated content was reviewed, refined, and incorporated into the application's workflows as appropriate. The platform's training workflows, assessment functionality, scoring, tracking, campaign management, gamification, dashboards, and integrations were developed as part of the project.

---

### 🎓 **Mandatory Training:**
Mandatory Training delivers organization-specific policy, security, and compliance training that employees are required to complete during onboarding and throughout their employment. The platform follows a structured video → assessment → completion workflow, enabling organizations to monitor both employee engagement with the training content and their understanding of the material.

Examples of mandatory training include:
- Clear Desk Policy
- Acceptable Use Policy
- Information Security Policies
- New Employee Onboarding
- Periodic Policy Refreshers
- Quarterly Mandatory Training

The Mandatory Training dashboard provides administrators with visibility into key training metrics, including:
- Training completion rates
- Assessment scores and pass rates
- Video viewing progress
- Outstanding or overdue training
- Employee-level completion status

Each employee receives a focused learning experience by viewing their assigned training content and completing the corresponding assessment. The platform records their progress, assessment results, and completion status, providing administrators with a clear view of training compliance across the organization.

---

### 🛡️ **Phishing Awareness:**
Phishing Awareness provides educational content designed to help employees understand how cyberattacks work and how to recognize, avoid, and respond to common threats.

Example topics include:
- Ransomware
- Man-in-the-Middle attacks
- Business Email Compromise
- Credential phishing
- Social engineering
- Malicious links and attachments
- Other current threat techniques

The platform supports awareness content relevant to both regional and global threat landscapes. Awareness campaigns track video engagement, completion status, and assessment results for each individual recipient.

---

### 🎣 **Phishing Campaigns:**
The phishing-simulation component enables security teams to conduct controlled, authorized simulations and measure how employees respond to realistic phishing scenarios. Campaigns can simulate common attack techniques, including:
- Malicious links
- Malicious attachments
- Display-name spoofing
- Typosquatted domains
- Credential-harvesting scenarios
- QR-code phishing
- Business Email Compromise
- Cloud-sharing lures
- MFA-fatigue scenarios

Each recipient has an individual tracking record that captures key campaign activity, from ```Delivered → Opened → Clicked → Submitted → Reported```. Simulation failures can automatically trigger remedial training, followed by reminders and escalation workflows to reinforce security awareness. The phishing functionality is intended exclusively for authorized security-awareness and security-testing environments.

---

### 🖥️ **IT Training:**
CyberLure also includes skills-based IT and cybersecurity training, divided into two areas:

#### 1. IT Generic Training:
Foundational subjects designed to build core IT and cybersecurity knowledge, including:
- Networking Fundamentals
- Information Security Fundamentals
- IT Fundamentals

Where appropriate, the platform can recommend relevant certification pathways such as CompTIA ITF+, A+, and Security+.

#### 2. IT Specific Training:
More specialized technical subjects focused on practical IT and cybersecurity skills, including:
- Packet Analysis with Wireshark
- Network Security
- Security Monitoring

---

### 🎮 **Gamification:**
The Games Hub provides interactive security-awareness exercises that reinforce concepts introduced through security training and phishing simulations. The games are organized into three progressive tiers, covering core cybersecurity skills, a broader range of threats, and behaviour-based security judgement.

#### Tier 1 · Core Skills
🎣 Spot the Phish — Identify whether simulated emails are legitimate or phishing attempts.
🔗 Link Inspector — Analyse URLs and determine whether they are safe or malicious.
🛡️ Password Fortress — Create strong passwords and see how quickly they could be cracked.
⚡ Cyber Quiz Blitz — Test cybersecurity knowledge through a fast-paced 10-question quiz.
📱 Smishing Challenge — Identify fraudulent and malicious SMS messages.

#### Tier 2 · Threat Variety
🔳 QR Code Detective — Investigate QR codes and identify potentially malicious destinations.
🔐 MFA Fatigue Defender — Learn how to respond safely to unexpected MFA approval requests.
☁️ OAuth Consent Check — Assess application permissions and identify excessive access requests.
📂 USB Drop Dilemma — Make the right security decision when encountering an unknown USB device.

#### Tier 3 · Behaviour & Judgement
🕵️ Insider Threat Watch — Distinguish between normal and potentially suspicious employee behaviour.
📄 Data Classification — Classify information according to its sensitivity and handling requirements.
🧠 Deepfake Detective — Identify whether audio, video, or images are genuine or AI-generated.

---

## 🧩 **Additional Capabilities:**

### 📊 **Dashboards & Human-Risk Analytics:**
A core objective of CyberLure is to move beyond simply measuring who clicked a phishing email and provide a broader view of organizational human risk. The platform brings together training, assessment, phishing, and behavioral data to provide organization-wide human-risk analytics.

The dashboards provide visibility into:
- Overall human-risk score
- Risk-band distribution
- Phishing engagement
- Click and reporting trends
- Training compliance
- Assessment performance
- Security champions
- Individual user risk
- Remediation status

Administrators can drill down to the individual-user level to review training assignments, video progress, assessment attempts and scores, phishing activity, and remediation status. Employees also have access to a personal, password-less Security Hub where they can view their assigned activities and security-readiness information.

### 📈 Reporting:
CyberLure provides both executive-level and detailed operational reporting, enabling leadership and security teams to view human-risk information at the level most relevant to them. Executive Reporting provides leadership with a high-level overview of:
- Human-risk posture
- Training compliance
- Phishing engagement
- Risk distribution
- Organizational trends
- Detailed Reporting

Provides security and operational teams with recipient-level details, including outstanding training, assessment results, phishing activity, and remediation requirements, with CSV export capabilities for further analysis.

### ⚙️ **Administration & Integrations:**
The administration layer provides centralized management of users, roles, permissions, and external platform integrations as below:
- User management
- Role-based access control
- Administrative permissions
- Integrations
  - SMTP — Email delivery
  - LDAP / Active Directory — Directory-based user import
  - NTP — Time synchronization
 
---

## 🧠 **Key Engineering Takeaways:**

CyberLure demonstrates the integration of cybersecurity, software engineering, automation, and analytics into a single working platform.

Security Engineering

Modelled real-world phishing and social-engineering techniques into controlled simulations and educational exercises.

Full-Stack Engineering

Designed and implemented the application's backend, database model, frontend, workflows, dashboards, reporting, and administrative interfaces.

Human-Risk Analytics

Converted behavioural and training signals into an organizational and individual human-risk model.

Workflow Automation

Connected phishing behaviour directly to remediation:

Detect → Assign → Train → Assess → Verify → Re-measure

Identity & Directory Integration

Implemented RBAC and LDAP/Active Directory integration to support organizational user management.

Offline-First Design

Designed the application to minimize external dependencies and support isolated or air-gapped environments.

AI-Assisted Development

Used Claude Code and AI-assisted development workflows during implementation for software engineering support, troubleshooting, content generation, and assessment-question creation.

For training assessments specifically, AI was used to generate an initial questionnaire based on the content of the training videos. The generated material was then reviewed, adapted, and integrated into the application's assessment workflow.

🔐 Security & Privacy

This repository is a portfolio and demonstration project.

All screenshots and example records use synthetic data and fictional identities such as @acme.example.

No real employee information is included.
No real credentials are included.
No real personal data is included.
Phishing scenarios are simulated.
The phishing functionality is intended only for authorized security-awareness and testing environments.
🚀 Project Summary

CyberLure demonstrates a complete security-awareness lifecycle:

Educate → Simulate → Measure → Remediate → Verify → Improve

Rather than treating awareness training and phishing simulations as separate activities, the platform connects them into a continuous feedback loop where employee behaviour can drive targeted training and measurable risk reduction.

The project combines cybersecurity domain knowledge, full-stack development, identity integration, workflow automation, analytics, gamification, and AI-assisted development into a single self-hosted platform designed for real-world organizational environments.


All screenshots and example records use synthetic data and fictional identities such as @acme.example. No real employee information, credentials, or personal data are included.

The phishing functionality is intended for authorized security-awareness and testing environments only.
