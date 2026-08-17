# 🛡️ CyberLure: A Phishing Simulation & Security Awareness Platform
> ##### (Mandatory Training · Phishing Awareness · Phishing Campaigns · IT Training · Gamification)



## 🎯 Objective

Most security incidents start with a person, not a firewall. The goal of CyberLure was to build — from the ground up — a single platform that lets a security team **train employees, safely phish them to test that training, remediate the ones who fall for it, and prove the human-risk needle is moving** — without depending on any external SaaS or internet connectivity.

The platform closes the full loop:

**Train → Simulate a phish → Track who clicks → Auto-assign remedial training → Verify it was watched & passed → Issue a certificate → Re-measure risk.**

---

## 🧰 Tech Stack

| Layer | Technology |
|---|---|
| **Backend** | Python · Flask · SQLAlchemy |
| **Database** | SQLite (zero-dependency default) · PostgreSQL/MySQL-ready |
| **Frontend** | Jinja2 · vanilla JavaScript · inline SVG (no CDN — offline-safe) |
| **Auth & Directory** | Session auth + role-based access control · LDAP/Active Directory (ldap3) |
| **Email** | SMTP delivery · open/click tracking pixels & per-recipient tokens |
| **Certificates** | Headless Chromium → PDF generation |
| **AI (optional)** | Anthropic Claude API for content assistance, with a deterministic offline fallback |
| **Deployment** | Runs on a single host · **offline / air-gapped mode** for regulated networks |

---

## 📊 Platform Overview:

CyberLure combines five major capabilities:

1. **Mandatory Training** — organization-relevant policy training employees must complete, at onboarding and on an ongoing basis.
2. **Phishing Awareness** — awareness videos on cyber-attack topics and the current regional & global threat landscape.
3. **Phishing Campaigns** — simulated phishing emails that test how employees respond to malicious links and attachments.
4. **IT Training** — generic and specialised IT/security skills training, with certification guidance.
5. **Gamification** — interactive security games (*Spot the Phish*, *Link Inspector*, and more).

These five capabilities are backed by **dashboards**, **executive & detailed reporting**, and **administration** (users/roles and email/LDAP/NTP integration).

---

## 1️⃣ Mandatory Training

Organization-relevant policy training that employees are required to complete, delivered as a video plus a graded assessment with completion tracking.

- **Onboarding** — mandatory videos new employees watch during induction.
- **Ongoing** — refreshers when a new policy is introduced, periodic refreshers of important existing policies, and quarterly-mandated training for all staff.
- **Relevant to the organization** — e.g. **Clear Desk Policy**, **Acceptable Use Policy**, etc.

The Mandatory Training dashboard shows completion, pass rates and video-watch progress across the workforce; each employee gets a focused "watch the video, then take the assessment" experience.

[![Mandatory training dashboard](images/08-mandatory-training.png)](images/08-mandatory-training.png)

[![Training experience](images/05-training-experience.png)](images/05-training-experience.png)

---

## 2️⃣ Phishing Awareness

Awareness training on how attacks actually work, kept current with the threat landscape.

- **Attack-topic videos** — known techniques such as **ransomware**, **man-in-the-middle**, business email compromise, and more.
- **Current threats** — content aligned to attacks prevalent **regionally (local)** and **internationally (global)**.
- **Compliance-driven** — awareness videos mandated by the **UAE Cyber Security Council** for **Cybersecurity Awareness Month**.

A dedicated Phishing Awareness dashboard tracks engagement and completion, and each awareness campaign tracks video-watch % and assessment results per recipient.

[![Phishing awareness dashboard](images/14-phishing-awareness.png)](images/14-phishing-awareness.png)

[![Awareness campaign detail](images/11-campaign-detail.png)](images/11-campaign-detail.png)

---

## 3️⃣ Phishing Campaigns

Simulated phishing emails sent to employees to **test their awareness and measure real behaviour**. Campaigns exercise the two classic failure actions:

- 🔗 **Clicking on links**
- 📎 **Clicking on / downloading attachments**

Every recipient is tracked individually — opened, clicked, submitted credentials, or reported — feeding a live behaviour funnel. Anyone who falls for a simulation is **automatically enrolled in remedial training**, with reminders and manager escalation.

[![Phishing campaigns dashboard](images/09-phishing-campaigns.png)](images/09-phishing-campaigns.png)

[![Phishing campaign detail — behaviour funnel & per-recipient tracking](images/16-phishing-campaign-detail.png)](images/16-phishing-campaign-detail.png)

---

## 4️⃣ IT Training

Skills-based IT and security training, delivered in two flavours:

- **IT Generic Training** — foundational topics, e.g. **Networking Fundamentals**, **Information Security Fundamentals** (with recommended certification paths such as CompTIA ITF+/A+/Security+ shown to learners who don't pass).
- **IT Specific Training** — specialised, hands-on topics, e.g. **Packet Analysis with Wireshark**, **Network Security & Monitoring**.

[![IT Generic training](images/17-it-training-generic.png)](images/17-it-training-generic.png)

[![IT Specific training](images/18-it-training-specific.png)](images/18-it-training-specific.png)

---

## 5️⃣ Gamification

Learning reinforced through a no-login **Games Hub** — a low-pressure way to build phishing instincts that map directly to the real simulations.

- **Spot the Phish** — realistic inbox messages across easy → medium → hard rounds, teaching 20+ techniques (typosquatting, homoglyphs, BEC, MFA-fatigue, quishing, cloud-share lures, …).
- **Link Inspector** — judge whether a web address is safe or malicious.
- …and more (quiz and password games).

[![Games Hub](images/03-games-hub.png)](images/03-games-hub.png)

[![Spot the Phish](images/04-spot-the-phish.png)](images/04-spot-the-phish.png)

[![Link Inspector](images/20-link-inspector.png)](images/20-link-inspector.png)

---

## ➕ Additional Features

### 📊 Dashboards & Analytics
Progress and status for **every candidate across every component**, rolled up into organization-wide human-risk analytics: a single human-risk score, risk-band distribution, security-champion leaderboards, click/report trends and compliance status. A per-user drill-down shows every training assigned to a person with video progress, assessment attempts, scores and follow-up state — and each employee gets a personal, password-less **Security Hub**.

[![Overall dashboard](images/06-overall-dashboard.png)](images/06-overall-dashboard.png)

[![Executive dashboard](images/07-executive-dashboard.png)](images/07-executive-dashboard.png)

[![Per-user attempts](images/10-per-user-attempts.png)](images/10-per-user-attempts.png)

[![Employee access & certificates](images/12-employee-access.png)](images/12-employee-access.png)

[![Personal Security Hub](images/02-personal-hub.png)](images/02-personal-hub.png)

### 📈 Reports
Both **executive** (leadership-ready summary) and **detailed** (per-recipient defaulter list with CSV export) reporting.

[![Executive report](images/13-reports-executive.png)](images/13-reports-executive.png)

[![Detailed report — defaulter list](images/24-reports-detailed.png)](images/24-reports-detailed.png)

### ⚙️ Settings & Administration
- **Users & Roles** — create users and role-based access control.
- **Integrations** — **Email (SMTP)**, **LDAP/Active Directory** (auto-import recipients), and **NTP**.

[![Settings — users & roles](images/21-settings-users.png)](images/21-settings-users.png)

[![Settings — email/SMTP integration](images/22-settings-email.png)](images/22-settings-email.png)

---

## 🧠 Key Takeaways

- Built a **complete security-awareness platform** end-to-end — five integrated components (Mandatory Training, Phishing Awareness, Phishing Campaigns, IT Training, Gamification) plus dashboards, reporting and administration — demonstrating both **security domain expertise** and **full-stack engineering**.
- Modelled **real adversary techniques** (BEC, homoglyphs, quishing, MFA-fatigue, credential harvesting) into safe, teachable simulations and games.
- Turned employee behaviour into a **measurable, defensible human-risk score** leadership can act on, with an automated **detect → train → verify** remediation loop.
- Engineered for the real world: **offline-capable, dependency-light, LDAP-integrated and privacy-conscious** by design.

---

<sub>All screenshots use synthetic demo data (fictional employees at <code>@acme.example</code>). No real personal data is shown.</sub>


All screenshots and example records use synthetic data and fictional identities such as @acme.example. No real employee information, credentials, or personal data are included.

The phishing functionality is intended for authorized security-awareness and testing environments only.
