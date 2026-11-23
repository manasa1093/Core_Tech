# 🛡️ AI Job & Internship Scam Shield

An AI-powered multi-agent system designed to investigate suspicious job postings, companies, and application links to help job seekers identify potential recruitment scams before they apply.

## 📌 About the Project

Job seekers often come across fake job postings, fraudulent recruiters, impersonated companies, suspicious application links, and offers that request money or personal information. Identifying these scams manually can be difficult.

**AI Job & Internship Scam Shield** aims to automate this investigation process using a multi-agent architecture. Multiple specialized agents analyze job details, company credibility, and digital threats, while a central orchestrator coordinates the investigation and generates an evidence-based risk report.

## 🎯 Objectives

- Detect potentially fraudulent job and internship postings.
- Investigate company legitimacy and recruiter credibility.
- Identify suspicious links and digital threats.
- Analyze scam indicators using AI-assisted reasoning.
- Generate an understandable risk score and investigation report.
- Maintain investigation history for registered users.

## 🏗️ System Architecture

React Dashboard → Spring Boot Backend → Multi-Agent Investigation → Risk Assessment → MySQL Database → Results Dashboard

### 🤖 AI Agent System

The system is designed around four specialized agents coordinated by a central orchestrator.

#### 1. Job Posting Investigator
- Analyzes job descriptions and recruitment messages.
- Identifies suspicious salary claims, unrealistic offers, urgency tactics, and unusual recruitment requirements.
- Extracts important job-related details and potential scam indicators.

#### 2. Company Intelligence Agent
- Investigates company information and credibility.
- Checks company identity, website, and available public information.
- Identifies possible company impersonation or inconsistencies.

#### 3. Digital Threat Agent
- Analyzes URLs, email domains, and application links.
- Identifies suspicious links, phishing indicators, and potential digital threats.
- Integrates with external threat intelligence services where available.

#### 4. Risk Assessment & Report Agent
- Combines findings from the other agents.
- Evaluates the evidence collected during the investigation.
- Generates a risk score, risk level, verdict, and explanation.
- Produces a consolidated investigation report.

### ⚙️ Investigation Orchestrator

The Investigation Orchestrator coordinates the entire process.

- Initiates the investigation.
- Executes specialized agents.
- Coordinates parallel agent execution.
- Tracks agent execution status.
- Handles failures and unavailable external services.
- Aggregates agent findings.
- Sends consolidated findings to the Risk Assessment Agent.

## 🔄 Investigation Workflow

1. The user submits a job posting, company details, recruiter information, or application link.
2. The React frontend sends the request to the Spring Boot backend.
3. The Investigation Orchestrator starts the investigation.
4. The Job Posting Investigator analyzes the recruitment content.
5. The Company Intelligence Agent investigates the company.
6. The Digital Threat Agent evaluates suspicious links and digital indicators.
7. The agents return their findings to the orchestrator.
8. The Risk Assessment Agent evaluates the collected evidence.
9. A consolidated risk score, verdict, and explanation are generated.
10. The investigation details and findings are stored in MySQL.
11. The dashboard displays the investigation results.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| React | Frontend development |
| JavaScript | Frontend logic |
| Java 17 | Backend development |
| Spring Boot 3.4.5 | REST API and backend architecture |
| Spring AI | AI integration and agent-based workflows |
| Spring Security | Security and authentication framework |
| Spring Data JPA | Database persistence |
| Hibernate | ORM |
| MySQL | Relational database |
| Maven | Build and dependency management |
| REST APIs | Frontend-backend communication and external integrations |

## 🧩 Backend Architecture

The backend follows a modular architecture designed to separate responsibilities.

- **Controller:** Handles REST API requests.
- **Service:** Implements investigation workflows and business logic.
- **Orchestrator:** Coordinates multiple investigation agents.
- **Agents:** Perform specialized investigation tasks.
- **Agent Tools:** Connect agents to external APIs and investigation utilities.
- **Repository:** Handles database operations.
- **Entity:** Defines database models.
- **DTO:** Handles request and response data.
- **Configuration:** Handles application, AI, and security configurations.
- **Exception Handling:** Handles errors and failed investigations.

## 🗂️ Planned Backend Modules

```text
job-scam-shield-api/
│
├── controller/
│   └── InvestigationController.java
│
├── service/
│   └── InvestigationService.java
│
├── orchestrator/
│   └── InvestigationOrchestrator.java
│
├── agents/
│   ├── JobPostingAgent.java
│   ├── CompanyIntelligenceAgent.java
│   ├── DigitalThreatAgent.java
│   └── RiskAssessmentAgent.java
│
├── tools/
│   └── AgentToolService.java
│
├── repository/
│
├── entity/
│
├── dto/
│
├── config/
│
├── exception/
│
└── JobScamShieldApplication.java
```

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/investigations` | Start a new investigation |
| GET | `/api/investigations` | Retrieve investigation history |
| GET | `/api/investigations/{id}` | Retrieve investigation details |

## 🗄️ Database Design

The database is designed to store investigation history, agent executions, individual findings, and final reports.

### Planned Tables

- **investigations** – Stores investigation details and status.
- **agent_execution** – Tracks individual agent execution, status, and timing.
- **agent_findings** – Stores findings, evidence, and investigation details from individual agents.
- **investigation_reports** – Stores the final risk score, verdict, and consolidated report.

## 📊 Investigation Results

The dashboard is intended to display:

- Overall risk score.
- Risk classification.
- Final investigation verdict.
- Agent-wise findings.
- Supporting evidence.
- Suspicious indicators.
- Investigation status.
- Previous investigation history.

## 🔌 External Integrations

The system is designed to integrate with external services for additional verification and investigation capabilities, such as:

- URL reputation and threat intelligence services.
- Company and website verification sources.
- Public web search and information sources.
- AI APIs through Spring AI.

External integrations depend on API availability, access permissions, and configuration.

## 🚀 Future Enhancements

- AI-powered agent orchestration using Spring AI.
- Real-time investigation progress tracking.
- Integration with external threat intelligence APIs.
- Advanced company identity verification.
- Improved evidence-based risk scoring.
- User authentication and investigation history.
- Detailed analytics and investigation dashboard.
- Improved handling of unavailable tools and agent failures.

## 💡 Why This Project?

The project focuses on improving online job-search safety by combining AI, backend engineering, external verification tools, and multi-agent collaboration into a practical application.

Instead of relying on a single prediction, the system is designed to investigate multiple aspects of a recruitment opportunity and generate a report based on collected evidence.

---

**Project Name:** AI Job & Internship Scam Shield  
**Backend:** Java 17 | Spring Boot 3.4.5 | Spring AI | MySQL  
**Frontend:** React | JavaScript  
**Architecture:** Multi-Agent AI Investigation System
