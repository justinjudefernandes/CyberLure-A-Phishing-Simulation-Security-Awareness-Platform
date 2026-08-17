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

### 🎣 **Phishing Campaigns:**
The phishing-simulation component enables security teams to conduct controlled, authorized simulations and measure how employees respond to realistic phishing scenarios. Campaigns can simulate common attack techniques, including:
🔗 Malicious links
📎 Malicious attachments
🎭 Display-name spoofing
🌐 Typosquatted domains
🔐 Credential-harvesting scenarios
📱 QR-code phishing
🏢 Business Email Compromise
☁️ Cloud-sharing lures
🔔 MFA-fatigue scenarios

Each recipient has an individual tracking record that captures key campaign activity, from ```Delivered → Opened → Clicked → Submitted → Reported```. Simulation failures can automatically trigger remedial training, followed by reminders and escalation workflows to reinforce security awareness. The phishing functionality is intended exclusively for authorized security-awareness and security-testing environments.

4️⃣ IT Training

CyberLure also includes skills-based IT and cybersecurity training.

Training is divided into two areas:

IT Generic Training

Foundational subjects such as:

Networking Fundamentals
Information Security Fundamentals
IT fundamentals

Where appropriate, the platform can provide recommended certification pathways such as CompTIA ITF+, A+, or Security+.

IT Specific Training

More specialized technical subjects, such as:

Packet Analysis with Wireshark
Network Security
Security Monitoring







5️⃣ 🎮 Gamification

The Games Hub provides interactive security-awareness exercises designed to reinforce concepts covered by the training and phishing simulations.

Spot the Phish

Users analyse realistic simulated inbox messages across Easy, Medium, and Hard difficulty levels.

The game covers more than 20 phishing and social-engineering techniques, including:

Typosquatting
Homoglyph attacks
Business Email Compromise
MFA fatigue
Quishing
Cloud-sharing lures
Credential harvesting
Link Inspector

Users evaluate URLs and determine whether they appear safe or malicious.

Additional quiz and security-awareness games can be incorporated into the platform.



AI-Assisted Assessment Development

AI was used as a development and content-assistance tool during the creation of the training assessments.

After reviewing the training videos, I used Claude to generate an initial set of questionnaire and assessment questions based on the material covered. These questions were then incorporated into the application's assessment workflow and structured around the learning objectives of each module.

AI was therefore used to accelerate content creation, while the platform's training workflow, assessment functionality, scoring, tracking, and integration were developed as part of the project.






📊 Dashboards & Human-Risk Analytics

A core objective of CyberLure was to move beyond simply measuring who clicked a phishing email.

The platform aggregates training, assessment, phishing, and behavioural data into organization-wide human-risk analytics.

The dashboards provide visibility into:

Overall human-risk score
Risk-band distribution
Phishing engagement
Click and reporting trends
Training compliance
Assessment performance
Security champions
Individual user risk
Remediation status

Administrators can drill down into individual users to view their training assignments, video progress, assessment attempts, scores, phishing activity, and remediation state.

Employees also receive a personal, password-less Security Hub showing their assigned activities and readiness information.
















📈 Reporting

CyberLure provides both executive-level and detailed operational reporting.

Executive Reporting

Provides leadership with a high-level view of:

Human-risk posture
Training compliance
Phishing engagement
Risk distribution
Organizational trends
Detailed Reporting

Provides operational teams with per-recipient information, including outstanding training and remediation activities, with CSV export capabilities.







⚙️ Administration & Integrations

The administration layer provides centralized management of users, roles, and external integrations.

Users & Roles
User management
Role-based access control
Administrative permissions
Integrations
SMTP — email delivery
LDAP / Active Directory — directory-based user import
NTP — time synchronization







🧠 Key Engineering Takeaways

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
