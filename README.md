<div align="center">

<img width="100%" src="assets/header.svg" alt="Forsyth Famous O. — Cloud Infrastructure & DevOps Engineer" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3500&pause=1000&color=00C9A7&center=true&vCenter=true&width=900&lines=Cloud+Infrastructure+%26+DevOps+Engineer;6%2B+Years+in+Tech;Microsoft+Certified%3A+DevOps+Engineer+Expert;Azure+Administrator+%7C+Azure+Network+Engineer;9+Microsoft+Applied+Skills+Credentials;Docker+%7C+Kubernetes+%7C+Terraform+%7C+Linux;Automate+everything.+Document+everything." alt="Cloud Infrastructure & DevOps Engineer, Azure certified, Docker, Kubernetes, Terraform, Linux" />

</div>

---

# 👋 About Me

I'm a **Cloud Infrastructure & DevOps Engineer** based in **Poland** with **6+ years in tech** (since 2020), designing, securing and operating infrastructure for large-scale enterprise environments on **Microsoft Azure**. I specialise in Azure networking, identity and governance, container platforms, Infrastructure as Code and automated delivery pipelines, turning manual, error-prone operations into repeatable, auditable processes.

I believe good infrastructure is only as strong as its documentation. The repositories here are reference implementations and runbooks, written the way I'd hand them over to a team: reproducible, verified and easy to operate.

### 🔭 What I Do

- Design and operate secure **Azure** infrastructure: networking, identity, governance and monitoring
- Containerise and deploy workloads with **Docker** and **Kubernetes**
- Provision infrastructure as code with **Terraform**
- Build and maintain CI/CD pipelines with **GitHub Actions** and **Azure DevOps**
- Publish technical guides for engineers on [dev.to](https://dev.to/forsyth_famous_)

---

# 🚀 Career Impact Highlights

- **Infrastructure Automation:** Automated VM and Application Gateway provisioning with **Terraform** and CI/CD pipelines, cutting environment setup time from **2 days to 30 minutes**.
- **Secure Networking:** Designed **hub-spoke** network architectures with **private endpoints** across **5 Azure subscriptions**.
- **Edge Security:** Protected web workloads with **Azure Application Gateway WAF**, combining Microsoft-managed rule sets with custom rules and **rate limiting** to block malicious and abusive traffic.
- **Cost Optimisation:** Reduced compute spend by putting idle virtual machines on **deallocation and shutdown schedules**, so non-production capacity is paid for only when it's used.
- **Product Engineering:** Built and hardened **KONTA**, a production AI platform on **Google Cloud Run** with **100+** automated test files and **70+** merged pull requests.

---

# 🛡️ Core Competencies

- **Azure Administration:** Compute, storage, resource governance and day-to-day management tasks.
- **Identity & Access:** Microsoft Entra ID, RBAC and Active Directory Domain Services.
- **Security, Monitoring & Compliance:** Secure storage (Azure Files and Blob Storage), Azure Monitor, cloud security operations, and Microsoft Purview retention and eDiscovery.
- **Azure Networking:** Virtual networks, hybrid connectivity, load balancing, network security and private access to PaaS services.
- **DevOps & CI/CD:** Source control strategy, branching and pull-request workflows, build and release pipelines, and DevSecOps practices.
- **Containers:** Writing Dockerfiles, multi-container stacks with Docker Compose, and Kubernetes manifests.
- **Infrastructure as Code & Automation:** Terraform, YAML, Bash scripting and Makefile automation.
- **Linux Administration:** Day-to-day operations, shell tooling and troubleshooting.

---

# ⚙️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=azure,gcp,terraform,docker,kubernetes,githubactions,linux,ubuntu,bash,git,github,nginx,nodejs,ts,react,firebase,python,mysql,wordpress,vscode&perline=10" alt="Tech stack icons" />
</p>

| Domain | Tools & Platforms |
| :--- | :--- |
| **Cloud** | Microsoft Azure, Azure CLI, Azure Monitor, Microsoft Entra ID, Google Cloud Run, Secret Manager, Firestore |
| **Automation** | Power Automate, Bash, Makefile |
| **Containers & Orchestration** | Docker, Docker Compose, Kubernetes |
| **Infrastructure as Code** | Terraform, YAML |
| **CI/CD & Version Control** | GitHub Actions, Azure DevOps, Git, GitHub |
| **OS & Directory Services** | Linux (Ubuntu), Active Directory Domain Services |
| **Web & Apps** | TypeScript, React, Node.js / Express, Python, Nginx, MySQL, WordPress |

---

# 🧰 Featured Projects

### 💼 KONTA: AI Business OS <sub>🔒 private</sub>
> **An AI-assisted business ledger for small businesses, run from a web dashboard or WhatsApp**

KONTA tracks sales, orders, inventory, customers, debtors and expenses. Merchants can send a WhatsApp text or voice note, and AI turns it into a *proposal*. Nothing changes in the books until a person confirms it, and the change itself is made by deterministic code.

- **Platform:** Containerised with a multi-stage Docker build (non-root runtime and health check) and deployed on **Google Cloud Run**. A least-privilege service account reads secrets from **Secret Manager**, and Firestore is locked down with deny-all rules, so all data access goes through the server.
- **Security hardening:** WhatsApp webhook HMAC verification, API rate limiting, request size limits, CSP/HSTS security headers, input validation before building Firestore paths, and phone numbers masked in logs.
- **Reliability:** Idempotent webhook processing, bounded timeouts on AI and messaging calls with safe retry rules, durable inbound and outbound message logs, and transactional ledger writes with concurrency isolation.
- **Engineering practice:** 100+ automated test files running against both an in-memory database and the Firestore emulator. Every change ships through a pull request (70+ merged).
- **Tech Stack**: `TypeScript`, `React`, `Node.js / Express`, `Firestore`, `Google Cloud Run`, `Secret Manager`, `Docker`, `Gemini AI`, `WhatsApp Cloud API`

---

### 🐳 [Docker Compose WordPress Deployment](https://github.com/forsythfamous/Docker-Compose-WordPress-Deployment)
> **A multi-container WordPress + MySQL stack with Docker Compose**

Provisions, monitors and tears down a two-tier application with persistent volumes, service dependencies and port mapping. Every stage is verified with captured output.
- **Tech Stack**: `Docker Compose`, `MySQL 8.0`, `WordPress`, `Docker Desktop`

---

### ☸️ [Kubernetes Pod Manifest Architecture](https://github.com/forsythfamous/Kubernetes-Pod-Manifest-Architecture)
> **Kubernetes Pod specification: structure and API contract**

A reference Pod manifest that breaks down the Kubernetes API contract (apiVersion, kind, metadata and spec) and sets out conventions for clean, version-controlled manifests.
- **Tech Stack**: `Kubernetes`, `YAML`, `Nginx`, `Git`

---

### 📝 [YAML Ain't Markup Language](https://github.com/forsythfamous/Yaml-Aint-Markup-Language)
> **YAML patterns for DevOps & Cloud Engineering**

A structured reference covering mappings, sequences, scalar types, multiline strings, anchors and aliases, followed by real-world GitHub Actions and app-config examples.
- **Tech Stack**: `YAML`, `GitHub Actions`, `VS Code`

---

### 🚀 [Nginx on Alpine: Container Image](https://github.com/forsythfamous/my-nginx-Dockerfile)
> **A lean Nginx image for serving static content**

A minimal Alpine-based image with a clean web root and documented build directives, covering layer caching, port mapping and container-lifecycle troubleshooting.
- **Tech Stack**: `Docker`, `Nginx`, `Alpine Linux`, `HTML`

---

### 🔁 [LoopCart: Git & CI/CD Workflow](https://github.com/forsythfamous/loopcart-remote)
> **An end-to-end team Git & delivery workflow**

Implements feature branching, conventional commits, pull requests, applying code-review feedback, merging to main and triggering a CI/CD pipeline.
- **Tech Stack**: `Git`, `GitHub`, `Python`, `Bash`

---

### 🛠️ More Projects

| Project | Description |
| :--- | :--- |
| [devops-lab](https://github.com/forsythfamous/devops-lab) | A Node.js app containerised with Docker, with build and run automated through a Makefile |
| [simple-container-lab](https://github.com/forsythfamous/simple-container-lab) | Container build-and-ship workflow for a Node.js service, from `docker build` to `git push` |
| [DevOps-Workstation-Setup](https://github.com/forsythfamous/DevOps-Workstation-Setup) | A standardised DevOps workstation baseline: Git, Azure CLI, Docker, Terraform and VS Code |

---

# ✍️ Latest Articles on dev.to

I publish practical Azure implementation guides for engineers and teams.

| Article | Topic |
| :--- | :--- |
| [How to Configure Azure Virtual Networks and Subnets for Virtual Machine Deployment](https://dev.to/forsyth_famous_/how-to-configure-azure-virtual-networks-and-subnets-for-virtual-machine-deployment-1g89) | Networking |
| [How to Secure Azure Storage Using Managed Identities and RBAC](https://dev.to/forsyth_famous_/how-to-secure-azure-storage-using-managed-identities-and-rbac-57m) | Security |
| [How to Configure Azure File Shares for Secure Enterprise File Storage](https://dev.to/forsyth_famous_/how-to-configure-azure-file-shares-for-secure-enterprise-file-storage-1hp4) | Storage |
| [How to Secure Private Documents with Azure Blob Storage](https://dev.to/forsyth_famous_/how-to-secure-private-documents-with-azure-blob-storage-step-by-step-azure-guide-1i6i) | Storage |
| [How to Host a Public Website Using Azure Blob Storage](https://dev.to/forsyth_famous_/how-to-host-a-public-website-using-azure-blob-storage-17ad) | Storage |
| [How to Deploy a Linux Virtual Machine in Microsoft Azure and Connect Using SSH](https://dev.to/forsyth_famous_/how-to-deploy-a-linux-virtual-machine-in-microsoft-azure-and-connect-using-ssh-3ah7) | Compute |
| [How to Prepare Your Azure Environment for Management and Administration Tasks](https://dev.to/forsyth_famous_/how-to-prepare-your-azure-environment-for-management-and-administration-tasks-2ea9) | Administration |

<p align="center">
  <a href="https://dev.to/forsyth_famous_"><img src="https://img.shields.io/badge/Read_more_on-dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white" alt="Read more on dev.to" /></a>
</p>

---

# 📜 Certifications & Credentials

<p align="center">
  <a href="https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/certification/devops-engineer"><img src="https://img.shields.io/badge/AZ--400-DevOps_Engineer_Expert-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-400" /></a>
  <a href="https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/certification/azure-administrator"><img src="https://img.shields.io/badge/AZ--104-Azure_Administrator-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-104" /></a>
  <a href="https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/certification/azure-network-engineer-associate"><img src="https://img.shields.io/badge/AZ--700-Azure_Network_Engineer-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-700" /></a>
</p>

### 🏅 Microsoft Certifications

| Certification | Exam | Earned | Verify |
| :--- | :---: | :---: | :---: |
| Microsoft Certified: DevOps Engineer Expert | AZ-400 | Jun 2026 | [🔗](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/certification/devops-engineer) |
| Microsoft Certified: Azure Administrator Associate | AZ-104 | Feb 2026 | [🔗](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/certification/azure-administrator) |
| Microsoft Certified: Azure Network Engineer Associate | AZ-700 | Jun 2025 | [🔗](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/certification/azure-network-engineer-associate) |

### 🧩 Microsoft Applied Skills

| Credential | Area |
| :--- | :--- |
| [Configure secure access to your workloads using Azure networking](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/configure-secure-workloads-use-azure-virtual-networking) | Networking |
| [Secure storage for Azure Files and Azure Blob Storage](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/secure-storage-azure-files-azure-blob-storage) | Storage & Security |
| [Deploy and configure Azure Monitor](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/deploy-and-configure-azure-monitor) | Observability |
| [Get started with cloud security and monitoring tasks](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/get-started-with-cloud-security-and-monitoring-tasks) | Security |
| [Get started with Azure management tasks](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/get-started-with-azure-management-tasks) | Administration |
| [Get started with identities and access using Microsoft Entra](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/get-started-with-identities-and-access-using-microsoft-entra) | Identity |
| [Administer Active Directory Domain Services](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/administer-active-directory-domain-services) | Identity |
| [Implement retention, eDiscovery, and Communication Compliance in Microsoft Purview](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/implement-retention-ediscovery-and-communication-compliance-in-microsoft-purview) | Compliance |
| [Create and manage automated processes by using Power Automate](https://learn.microsoft.com/en-us/users/forsythfamous-3964/credentials/applied-skill/create-and-manage-automated-processes-with-power-automate) | Automation |

---

# 🤝 Let's Connect

<p align="center">
  <a href="https://github.com/forsythfamous"><img src="https://skillicons.dev/icons?i=github" alt="GitHub" /></a>
  <a href="https://www.linkedin.com/in/forsythazure"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn" /></a>
  <a href="https://dev.to/forsyth_famous_"><img src="https://skillicons.dev/icons?i=devto" alt="dev.to" /></a>
</p>

- **Location:** Poland 🇵🇱
- **Professional Networking:** [LinkedIn](https://www.linkedin.com/in/forsythazure)
- **Technical Writing:** [dev.to/forsyth_famous_](https://dev.to/forsyth_famous_)
- **Credentials:** [Microsoft Learn Profile](https://learn.microsoft.com/en-us/users/forsythfamous-3964/)
- **Open to:** Cloud & DevOps collaboration, technical consulting and new opportunities

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=forsythfamous&color=00C9A7&style=for-the-badge&label=PROFILE+VIEWS" alt="Profile Views" />
  <img src="https://img.shields.io/github/followers/forsythfamous?label=Followers&style=for-the-badge&color=0B3D91&logo=github" alt="GitHub Followers" />
</p>

<p align="center">
  <b>Building reliable cloud infrastructure, one automated step at a time.</b>
</p>

<img width="100%" src="assets/footer.svg" alt="" />
