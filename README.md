# 🛡️ CyberLure: A Phishing Simulation & Security Awareness Platform
> ##### (Mandatory Training · Phishing Awareness · Phishing Campaigns · IT Training · Gamification)

## 🎯 Objective:
Security awareness is most effective when organizations can continuously educate, test, measure, and remediate employee behavior. The objective of CyberLure was to build a solution that would encompass the complete security-awareness lifecycle rather than a standalone phishing simulator:

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

### **The Security-Awareness Lifecycle:**

<img width="1000" height="300" alt="CyberLure_Security_Awareness_Lifecycle" src="https://github.com/user-attachments/assets/999f3c7b-ac87-426d-b68a-9592a6779883" />
<br/>

### **System Overview:**

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

📌 Refer to the below screenshots: (left to right)

<img width="390" height="230" alt="01-create-training-campaign" src="https://github.com/user-attachments/assets/4a54e7b0-9636-4572-83b3-6bfa52878871" />
<img width="390" height="230" alt="02-mandatory-training-dashboard" src="https://github.com/user-attachments/assets/6fac07cf-2410-4a29-b98f-d6590a85d845" />
<img width="390" height="230" alt="03-employee-email" src="https://github.com/user-attachments/assets/3f9bce95-4a8f-4638-8a4d-1a60a9cff9f9" />
<img width="390" height="230" alt="04-personal-dashboard" src="https://github.com/user-attachments/assets/afff3aec-cd18-4b00-a756-addbab7f8a0b" />
<img width="390" height="230" alt="05-training-video-player" src="https://github.com/user-attachments/assets/94ec277e-f773-424d-b4d2-e9a0812849bd" />
<img width="390" height="230" alt="06-video-progress-forward-cap" src="https://github.com/user-attachments/assets/1f61f377-112b-4a9d-a59a-0ffc2d331699" />
<img width="390" height="230" alt="07-assessment" src="https://github.com/user-attachments/assets/3b82621d-e8f6-418c-bdde-f9314948703c" />
<img width="390" height="230" alt="08-campaign-detail-progress" src="https://github.com/user-attachments/assets/818e94f5-0b5b-4bd8-b69a-a7d93246998d" />
<img width="785" height="350" alt="09-certificate-issued" src="https://github.com/user-attachments/assets/acbcfc37-e170-488d-8d6f-a81949f0130a" />

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

📌 Refer to the below screenshots: (left to right)

<img width="390" height="230" alt="01-create-awareness-campaign" src="https://github.com/user-attachments/assets/8e4b1af1-b7e2-4317-b0f1-96a685e8736c" />
<img width="390" height="230" alt="02-phishing-awareness-dashboard" src="https://github.com/user-attachments/assets/6141dbe7-60c9-41cd-988d-20910e53d2db" />
<img width="390" height="230" alt="03-awareness-email" src="https://github.com/user-attachments/assets/c230e916-f0ff-4d49-9928-b15ba9531f88" />
<img width="390" height="230" alt="04-personal-dashboard" src="https://github.com/user-attachments/assets/9f7b69f0-2a41-42c6-a77c-ea9796bcf7ee" />
<img width="390" height="230" alt="05-awareness-video-player" src="https://github.com/user-attachments/assets/9c2a7f97-1163-4e6d-9df0-8dc67f6f6e70" />
<img width="390" height="230" alt="06-video-progress-forward-cap" src="https://github.com/user-attachments/assets/50a2be99-407f-43d1-90df-4c54d26e76cd" />
<img width="390" height="230" alt="07-assessment" src="https://github.com/user-attachments/assets/3cd3b02a-830b-4b20-84d5-ef42dcea9a85" />
<img width="390" height="230" alt="08-awareness-campaign-detail-progress" src="https://github.com/user-attachments/assets/57128b8b-eb2c-4241-9135-103c593cb423" />
<img width="785" height="350" alt="09-certificate-issued" src="https://github.com/user-attachments/assets/318fc8f3-98c6-44ba-b06a-47e4442e922c" />

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

Each recipient has an individual tracking record that captures key campaign activity, from ```Delivered → Opened → Clicked → Submitted → Reported```

Employees can report a simulated phishing email by clicking the “Report Phishing” button. If the employee correctly identifies and reports the phishing email before falling for the simulation, they are redirected to a “Good Catch” page, reinforcing positive security behavior.

If the employee has already fallen for the simulated phishing attack and subsequently clicks the “Report Phishing” button, they are redirected to a page displaying: “Reporting is the right instinct — but this one had already caught you.” This reinforces that reporting remains the right action, while highlighting that the interaction with the simulated threat had already occurred.

Simulation failures can automatically trigger remedial training, followed by reminders and escalation workflows to reinforce security awareness. The phishing functionality is intended exclusively for authorized security-awareness and security-testing environments.

📌 Refer to the below screenshots: (left to right)

<img width="390" height="230" alt="01-create-phishing-campaign" src="https://github.com/user-attachments/assets/6ee64e6b-e2fb-414f-a6ce-89b0764e8506" />
<img width="390" height="230" alt="02-phishing-campaigns-dashboard" src="https://github.com/user-attachments/assets/495cb897-2931-4aff-b9e1-67fe4801313e" />
<img width="390" height="230" alt="03-lure-email" src="https://github.com/user-attachments/assets/ea61a173-432f-47b1-aac5-4f81356cdb2a" />
<img width="390" height="230" alt="05-phishing-education-page" src="https://github.com/user-attachments/assets/1c6d801c-073a-4ae9-88be-ef2e2ab638ec" />
<img width="390" height="230" alt="06-reported-good-catch" src="https://github.com/user-attachments/assets/cec027ec-133f-401f-85d1-10c2bc12e597" />
<img width="390" height="230" alt="07-reported-after-falling" src="https://github.com/user-attachments/assets/9f795193-708b-4f67-90c7-a96cfeaff932" />
<img width="785" height="350" alt="08-campaign-detail-behaviour-funnel" src="https://github.com/user-attachments/assets/fc206a01-ec57-47d7-ace4-a76eced5fbb4" />


### 🖥️ **IT Training:**
CyberLure also includes skills-based IT and cybersecurity training, divided into two areas:

#### 1. IT Generic Training:
Foundational subjects designed to build core IT and cybersecurity knowledge, including but not limited to:
- Networking Fundamentals
- Information Security Fundamentals
- IT Fundamentals

Where appropriate, the platform can recommend relevant certification pathways such as CompTIA ITF+, A+, and Security+.

📌 Refer to the below screenshots: (left to right)

#### 2. IT Specific Training:
More specialized technical subjects focused on practical IT and cybersecurity skills, including but not limited to:
- Packet Analysis with Wireshark
- Network Security
- Security Monitoring

📌 Refer to the below screenshots: (left to right)

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

📌 Refer to the below screenshots: (left to right)

<img width="260" height="230" alt="01-games-hub" src="https://github.com/user-attachments/assets/7c802615-798a-4912-9494-a703d373e52c" />
<img width="260" height="230" alt="02-spot-the-phish" src="https://github.com/user-attachments/assets/2b3c066a-2c8a-4bce-b0e0-a8ba75d0296a" />
<img width="260" height="230" alt="03-link-inspector" src="https://github.com/user-attachments/assets/1b36d2a0-28dc-4051-9aa5-af8065a4eb4f" />
<img width="260" height="230" alt="04-password-fortress" src="https://github.com/user-attachments/assets/88de57ac-7164-45f8-afce-ca0c23f7bd91" />
<img width="260" height="230" alt="05-cyber-quiz-blitz" src="https://github.com/user-attachments/assets/dc6b15af-4653-499a-add8-cdc621a11112" />
<img width="260" height="230" alt="06-smishing-challenge" src="https://github.com/user-attachments/assets/1e0a8a75-3728-4ab2-8af5-1f84d9bebc2c" />
<img width="260" height="230" alt="07-qr-code-detective" src="https://github.com/user-attachments/assets/5f5b9f2d-7372-487b-af5e-768fe6ae6cbb" />
<img width="260" height="230" alt="08-mfa-fatigue-defender" src="https://github.com/user-attachments/assets/ce56a7f1-ad68-4d42-8407-b181f8102b86" />
<img width="260" height="230" alt="09-oauth-consent-check" src="https://github.com/user-attachments/assets/46130132-f7a1-45b5-acad-13340f91a783" />
<img width="260" height="230" alt="10-usb-drop-dilemma" src="https://github.com/user-attachments/assets/71315748-994a-4f4e-96da-391115d1652f" />
<img width="260" height="230" alt="11-insider-threat-watch" src="https://github.com/user-attachments/assets/5f2bf306-3965-409d-ada5-604362109262" />
<img width="260" height="230" alt="12-data-classification" src="https://github.com/user-attachments/assets/6474913f-a68f-41f2-a31d-3eb5bc65fa6f" />
<img width="390" height="230" alt="13-deepfake-detective" src="https://github.com/user-attachments/assets/1dcb2a33-ca2b-4381-b152-6b29f5b50312" />
<img width="390" height="230" alt="14-Certificate" src="https://github.com/user-attachments/assets/8c694557-9492-4f1a-8747-ab40f743bfb7" />



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

📌 Refer to the below screenshots: (left to right)

### 📈 Reporting:
CyberLure provides both executive-level and detailed operational reporting, enabling leadership and security teams to view human-risk information at the level most relevant to them. Executive Reporting provides leadership with a high-level overview of:
- Human-risk posture
- Training compliance
- Phishing engagement
- Risk distribution
- Organizational trends
- Detailed Reporting

Provides security and operational teams with recipient-level details, including outstanding training, assessment results, phishing activity, and remediation requirements, with CSV export capabilities for further analysis.

📌 Refer to the below screenshots: (left to right)

### ⚙️ **Administration & Integrations:**
The administration layer provides centralized management of users, roles, permissions, and external platform integrations as below:
- User management
- Role-based access control
- Administrative permissions
- Integrations
  - SMTP — Email delivery
  - LDAP / Active Directory — Directory-based user import
  - NTP — Time synchronization

📌 Refer to the below screenshots: (left to right)
 
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
