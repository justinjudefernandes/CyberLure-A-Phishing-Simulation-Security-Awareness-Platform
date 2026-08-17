# 🛡️ CyberLure: A Phishing Simulation & Security Awareness Platform
> #### Phishing Simulations → Awareness Training → Gamified Learning → Human-Risk Analytics

CyberLure is a self-hosted security-awareness platform designed and developed to help organizations simulate phishing attacks, deliver targeted security training, reinforce learning through gamification, and measure human cyber risk.

The platform is designed with offline and air-gapped environments in mind, making it suitable for organizations operating in regulated or restricted networks.

🎯 Project Objective:

Many security incidents involve human behaviour — whether it is clicking a malicious link, opening an unsafe attachment, submitting credentials, or failing to recognize a social-engineering attempt.

I wanted to build a platform that could address the complete security-awareness lifecycle in one place:

Simulate → Measure → Train → Test → Remediate → Re-measure

CyberLure allows a security team to safely run phishing simulations against its own users, identify areas of weakness, automatically assign appropriate training, verify learning outcomes, and use behavioural data to measure changes in human risk.

The goal was not simply to build another phishing simulator, but to demonstrate how security awareness, behavioural data, automation, and analytics can work together as a single platform.

📊 Platform Overview

CyberLure combines four major capabilities:

🎣 Phishing Simulation

Create and manage realistic security-awareness campaigns using simulated scenarios such as:

Typosquatted domains
Display-name spoofing
Business Email Compromise (BEC)
Credential-harvesting scenarios
QR-code phishing (quishing)
Cloud-file sharing lures
Attachment-based scenarios
MFA-fatigue scenarios

Campaigns provide visibility into recipient behaviour, including delivery, opens, clicks, credential submissions, and reports.

🎓 Security Awareness Training

Deliver mandatory and phishing-awareness training through video-based modules followed by graded assessments.

The platform tracks:

Video-watch progress
Assessment attempts
Scores
Completion status
Training compliance
Certificates

For the assessment content, I used AI assistance to generate an initial questionnaire based on the training videos, then incorporated and structured the resulting questions within the platform.

🔁 Automated Remediation

The platform connects phishing-simulation results directly to training workflows.

For example:

User clicks simulated phishing email → remediation training assigned → reminders sent → assessment completed → certificate issued → risk re-evaluated

This creates a measurable feedback loop rather than treating phishing simulations as one-off exercises.

🎮 Gamified Learning

A dedicated Games Hub provides interactive security-awareness exercises.

The main game, Spot the Phish, presents simulated inbox messages across Easy, Medium, and Hard difficulty levels and teaches users to identify a range of real-world phishing and social-engineering techniques.

📈 Human-Risk Analytics

One of the key goals of the project was to move beyond simply reporting "who clicked?"

CyberLure combines behavioural and training signals to produce an individual and organizational human-risk score.

The dashboards provide visibility into areas such as:

Overall human-risk score
Risk-band distribution
Phishing engagement
Click and report trends
Training compliance
Assessment performance
Individual user risk
Security champions
Remediation status

This provides leadership with a more useful question than simply "How many people clicked?":

"Are our users becoming more resilient to social-engineering attacks?"

🧰 Technology Stack
Layer	Technology
Backend	Python · Flask · SQLAlchemy
Database	SQLite · PostgreSQL/MySQL-ready
Frontend	Jinja2 · Vanilla JavaScript · Inline SVG
Authentication	Session authentication · RBAC
Directory Integration	LDAP / Active Directory via ldap3
Email	SMTP · Tracking pixels · Tracking tokens
Certificates	Headless Chromium → PDF
AI Assistance	Anthropic Claude API with offline/deterministic fallback
Deployment	Single-host deployment · Offline / air-gapped capable

The frontend intentionally avoids CDN dependencies, allowing the application to operate in environments where external internet access is unavailable.

🛠️ Engineering & Security Capabilities Demonstrated

This project demonstrates practical experience across several areas:

Full-Stack Development

Designed and implemented the application's data model, backend services, workflows, UI, dashboards, and reporting.

Security Engineering

Translated real-world phishing and social-engineering techniques into safe simulations and educational exercises.

Human-Risk Modelling

Developed a weighted risk model using behavioural indicators such as phishing interactions, reporting behaviour, and training status.

Workflow Automation

Connected user behaviour to automated remediation workflows, reminders, escalation, training, assessment, and certification.

Identity & Directory Integration

Implemented role-based access control and LDAP/Active Directory integration for organizational user management.

Privacy & Offline-First Architecture

Designed the platform to minimize external dependencies and support isolated or air-gapped environments.

AI-Assisted Development

Used AI tools during development for software engineering assistance, troubleshooting, content generation, and questionnaire creation. The overall application architecture, integration, workflows, and implementation were developed and assembled as part of the project.

📁 Key Features
🎣 Phishing Campaign Builder — create simulated campaigns with realistic lures and per-recipient tracking
📊 Campaign Analytics — monitor delivery, opens, clicks, credential submissions, and reports
🎓 Security Awareness Training — video-based training with assessments and completion tracking
🔁 Automated Remediation — automatically assign targeted training following simulation failures
📝 AI-Assisted Questionnaires — generate initial assessment questions from training material and integrate them into learning modules
🏆 Gamified Learning — interactive Spot the Phish exercises across multiple difficulty levels
🧑‍💼 User Drill-Down — review individual training, assessment, phishing, and remediation activity
📈 Executive Dashboards — human-risk scoring, risk distribution, compliance, and behavioural trends
🪪 Certificates — generate PDF completion certificates
👤 Personal Security Hub — password-less employee portal for assigned training and readiness information
🔌 LDAP / Active Directory — organizational user import and directory integration
📧 SMTP Integration — campaign and training email delivery
🔐 RBAC — role-based administrative access
📴 Offline / Air-Gapped Mode — designed to operate without external SaaS dependencies

🔍 Platform Walkthrough
🔐 Sign-In

A self-hosted administrative console with no dependency on an external identity provider.




📈 Executive Overview & Human-Risk Analytics

The overall dashboard transforms behavioural and training data into an organizational view of human cyber risk.

It provides visibility into:

Human-risk score
Risk distribution
Security champions
Training compliance
Phishing engagement
Behavioural trends










🎯 Phishing Campaign Tracking

Campaign dashboards provide a behavioural funnel from delivery through engagement and simulated credential submission.

Administrators can also view individual recipient activity and follow-up status.










🧑‍💼 User Drill-Down & Certificates

Administrators can drill down into individual users to review:

Training assignments
Video-watch progress
Assessment attempts
Assessment scores
Remediation status
Certificate status
Phishing-simulation activity







🙋 Employee Experience

Each employee receives a personal Security Hub showing their assigned activities and readiness information.

The training workflow guides users through the training video and assessment.







🎮 Gamified Security Awareness

The Games Hub provides a lightweight way for users to practise identifying phishing attempts.

Spot the Phish uses realistic simulated inbox messages across multiple difficulty levels and covers 20+ phishing and social-engineering techniques.







🧠 Key Takeaways

CyberLure demonstrates my ability to combine cybersecurity knowledge, software engineering, automation, and analytics into a single working platform.

The project allowed me to explore and implement:

A complete phishing-simulation workflow
Security-awareness training and assessment
Automated user remediation
Gamified security education
Human-risk scoring and analytics
LDAP / Active Directory integration
SMTP-based communication workflows
Role-based access control
PDF certificate generation
Offline and air-gapped application design
AI-assisted software development and content creation

Most importantly, the project demonstrates a shift from simply measuring phishing clicks toward creating a continuous measure → educate → remediate → re-measure security-awareness cycle.

⚠️ Portfolio / Demo Disclaimer

This repository is a demonstration and portfolio project.

All screenshots and example records use synthetic data and fictional identities such as @acme.example. No real employee information, credentials, or personal data are included.

The phishing functionality is intended for authorized security-awareness and testing environments only.
