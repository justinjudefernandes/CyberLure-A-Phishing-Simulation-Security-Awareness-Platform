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

## 🏗️ Architecture:

CyberLure is a single self-hosted Flask application that runs the entire security-awareness lifecycle in one place — no external SaaS, and no internet dependency at runtime. The security team drives everything from the admin console; recipients interact only through emails, training pages, and games; and every interaction feeds a central tracking and scoring layer that powers the dashboards and the automated remediation loop.

**The Security-Awareness Lifecycle:**

<img width="1000" height="300" alt="CyberLure_Security_Awareness_Lifecycle" src="https://github.com/user-attachments/assets/999f3c7b-ac87-426d-b68a-9592a6779883" />

**System Overview:**

<img width="1000" height="300" alt="CyberLure_System_Overview" src="https://github.com/user-attachments/assets/36dde92b-d8ee-43d7-879a-f872dacc99ad" />

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

### 🎮 **Gamification:**
The Games Hub provides interactive security-awareness exercises that reinforce concepts introduced through security training and phishing simulations. The games are organized into three progressive tiers, covering core cybersecurity skills, a broader range of threats, and behavior-based security judgement.

#### Tier 1 · Core Skills
- 🎣 Spot the Phish — Identify whether simulated emails are legitimate or phishing attempts.
- 🔗 Link Inspector — Analyse URLs and determine whether they are safe or malicious.
- 🛡️ Password Fortress — Create strong passwords and see how quickly they could be cracked.
- ⚡ Cyber Quiz Blitz — Test cybersecurity knowledge through a fast-paced 10-question quiz.
- 📱 Smishing Challenge — Identify fraudulent and malicious SMS messages.

#### Tier 2 · Threat Variety
- 🔳 QR Code Detective — Investigate QR codes and identify potentially malicious destinations.
- 🔐 MFA Fatigue Defender — Learn how to respond safely to unexpected MFA approval requests.
- ☁️ OAuth Consent Check — Assess application permissions and identify excessive access requests.
- 📂 USB Drop Dilemma — Make the right security decision when encountering an unknown USB device.

#### Tier 3 · Behaviour & Judgement
- 🕵️ Insider Threat Watch — Distinguish between normal and potentially suspicious employee behaviour.
- 📄 Data Classification — Classify information according to its sensitivity and handling requirements.
- 🧠 Deepfake Detective — Identify whether audio, video, or images are genuine or AI-generated.

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
 
## 🔒 Security, Privacy & Responsible Use:
CyberLure sends simulated phishing and handles employee behavioural data, so it was built to be safe and self-contained by design.
- **Authorized use only** — the phishing functionality is intended exclusively for authorized, internal security-awareness and security-testing programmes.
- **Offline / air-gapped** — runs entirely on a single host with no external SaaS and no runtime internet dependency; sensitive data never leaves the organization's network.
- **Data privacy** — all training, assessment, and behavioural data stays in the local database; the AI features degrade gracefully to a deterministic offline generator when no API key is configured.
- **Role-based access control** — administrative functions, campaign management, and reporting are gated by roles and permissions.
- **Signed tracking tokens** — recipient links carry per-recipient signed tokens rather than exposing identifiers, and email-open/click tracking is scoped to the campaign.
- **No hardcoded secrets** — credentials and API keys are supplied via environment/settings, never committed to source.
- **Synthetic showcase data** — every screenshot in this repository uses fictional employees (@acme.example); no real personal data is shown.

## 🗺️ Roadmap / Future Enhancements:
- SSO / SAML authentication alongside the existing LDAP/AD integration.
- Multilingual content (e.g. English & Arabic) across training, assessments, and games.
- Expanded Tier 2 & Tier 3 games and additional scenario packs.
- Scheduled & recurring campaigns with automated cadence.
- REST API / SIEM export for feeding human-risk signals into existing security tooling.
- Containerized deployment (Docker Compose) for one-command self-hosting.

## 🧗 Challenges & Lessons Learned:
- **Offline video watch-tracking** — enforcing "watch the full video before the assessment" required a furthest-watched cap, resume-on-reload, and handling mobile-browser quirks (e.g. Chrome pausing timeupdate events during seeks) — all without any external video platform.
- **Reliable mobile playback** — a DevTools-detection heuristic was falsely pausing videos on phones (the browser's address bar tripped a window-size check); scoping it to desktop-only fixed legitimate playback.
- **A defensible human-risk score** — turning raw signals (clicks, reports, training gaps) into a single 0–100 score meant only counting phishing a user engaged with, so an unopened lure reads as "no signal" rather than false safety.
- **Air-gapped AI** — content assistance uses Claude when available but falls back to a deterministic generator, so the platform is fully functional with zero connectivity.
- **Bulletproof, offline email** — campaign and certificate emails render as inline-SVG, self-contained HTML (no CDN, no remote images) so they display consistently across mail clients on isolated networks.

## 🧠 Key Takeaways:
- Built a complete security-awareness platform end-to-end — five integrated capabilities (Mandatory Training, Phishing Awareness, Phishing Campaigns, IT Training, Gamification) plus dashboards, reporting, and administration — demonstrating both security domain expertise and full-stack engineering.
- Modelled real adversary techniques (BEC, homoglyphs, quishing, MFA-fatigue, credential harvesting, insider threat, deepfakes) into safe, teachable simulations and games.
- Turned employee behavior into a measurable, defensible human-risk score that leadership can act on, closed by an automated detect → train → verify remediation loop.
- Engineered for the real world: offline-capable, dependency-light, LDAP-integrated, and privacy-conscious by design.
