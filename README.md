<div align="center">

<img width="100%" src="assets/header.svg" alt="Forsyth Famous O. — Cloud Infrastructure & DevOps Engineer" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3500&pause=1000&color=00C9A7&center=true&vCenter=true&width=900&lines=Cloud+Infrastructure+%26+DevOps+Engineer;6%2B+Years+in+Tech;Microsoft+Certified%3A+DevOps+Engineer+Expert;Azure+Administrator+%7C+Azure+Network+Engineer;9+Microsoft+Applied+Skills+Credentials;Docker+%7C+Kubernetes+%7C+Terraform+%7C+Linux;Automate+everything.+Document+everything." alt="Cloud Infrastructure & DevOps Engineer, Azure certified, Docker, Kubernetes, Terraform, Linux" />

<a href="https://forsythfamous.pages.dev"><img src="https://img.shields.io/badge/Website-forsythfamous.pages.dev-22C55E?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Website: forsythfamous.pages.dev" /></a>

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
  <img src="https://skillicons.dev/icons?i=azure,gcp,terraform,docker,kubernetes,githubactions,linux,ubuntu,bash,git,github,nginx,nodejs,ts,react,astro,cloudflare,firebase,python,mysql,wordpress,vscode&perline=11" alt="Tech stack icons" />
</p>

| Domain | Tools & Platforms |
| :--- | :--- |
| **Cloud** | Microsoft Azure, Azure CLI, Azure Monitor, Microsoft Entra ID, Google Cloud Run, Secret Manager, Firestore, Cloudflare Pages |
| **Automation** | Power Automate, Bash, Makefile |
| **Containers & Orchestration** | Docker, Docker Compose, Kubernetes |
| **Infrastructure as Code** | Terraform, tflint, Trivy, YAML |
| **CI/CD & Version Control** | GitHub Actions, Azure DevOps, Git, GitHub |
| **OS & Directory Services** | Linux (Ubuntu), Active Directory Domain Services |
| **Web & Apps** | TypeScript, React, Node.js / Express, Python, Astro, Nginx, MySQL, WordPress |

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

### 🌐 [Azure Hub-Spoke Network in Terraform](https://github.com/forsythfamous/azure-hub-spoke) · [case study](https://forsythfamous.pages.dev/work/azure-hub-spoke/)
> **A private-by-default Azure network, changed only through a reviewed pipeline**

A hub VNet with central Private DNS and an optional Azure Firewall, a workload spoke behind Application Gateway WAF_v2, and a data spoke whose storage is reachable only through a private endpoint. Changes go through GitHub Actions: plan on every pull request, apply only after an approval gate, authenticated with OIDC federated credentials and no client secrets.

- **Security:** Storage public network access and shared keys disabled, per-subnet NSGs with explicit deny, no public IP on the backend VM, and WAF in Prevention mode (DRS 2.1 + Bot Manager) with an admin-path block and rate limiting.
- **Quality gates:** `terraform fmt`, `validate`, offline `terraform test` against a mocked provider, `tflint` (azurerm ruleset) and a `trivy config` scan on every change. Six ADRs record the design decisions.
- **Cost controls:** Optional firewall, App Gateway autoscaling from zero, a daily log ingestion cap and resource-group budgets.
- **Tech Stack**: `Terraform`, `Azure`, `Application Gateway WAF_v2`, `Azure Firewall`, `Private Endpoints`, `GitHub Actions`, `OIDC`, `tflint`, `Trivy`

---

### 🖥️ [This Portfolio: a site that operates itself](https://github.com/forsythfamous/portfolio) · [live site](https://forsythfamous.pages.dev)
> **A static site rebuilt, checked and deployed by its own pipeline**

An Astro site on Cloudflare Pages, rebuilt by GitHub Actions on every push and every night from the GitHub and dev.to APIs. The home page shows the site's own pipeline as a live diagram, and each case study includes an interactive architecture diagram generated at build time.

- **Security:** A strict Content Security Policy (`script-src` and `style-src` limited to `'self'`) with HSTS and other security headers. CI fails the build if any inline script or style appears.
- **Resilience:** Every data source is optional. A failing API shows up as a warning on the diagram instead of breaking the site.
- **Tech Stack**: `Astro`, `TypeScript`, `Cloudflare Pages`, `GitHub Actions`, `Wrangler`, `GitHub API`

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

# 🌍 Open Source Contributions

| Project | Contribution |
| :--- | :--- |
| [cloudcost-cli](https://github.com/raphgm/cloudcost-cli) | [Added a `findings summary` command](https://github.com/raphgm/cloudcost-cli/pull/27) that rolls up FinOps policy findings per Azure resource and ranks them by combined cost impact, so teams know which resource to fix first |

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
  <a href="https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/5BAAF193E17745D8?sharingId=AE41C8CE11434D50"><img src="https://img.shields.io/badge/AZ--400-DevOps_Engineer_Expert-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-400" /></a>
  <a href="https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/DF92838DC9D2E7C0?sharingId=AE41C8CE11434D50"><img src="https://img.shields.io/badge/AZ--104-Azure_Administrator-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-104" /></a>
  <a href="https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/C1CC44551BE33731?sharingId=AE41C8CE11434D50"><img src="https://img.shields.io/badge/AZ--700-Azure_Network_Engineer-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="AZ-700" /></a>
</p>

### 🏅 Microsoft Certifications

| Certification | Exam | Earned | Verify |
| :--- | :---: | :---: | :---: |
| Microsoft Certified: DevOps Engineer Expert | AZ-400 | Jun 2026 | [🔗](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/5BAAF193E17745D8?sharingId=AE41C8CE11434D50) |
| Microsoft Certified: Azure Administrator Associate | AZ-104 | Feb 2026 | [🔗](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/DF92838DC9D2E7C0?sharingId=AE41C8CE11434D50) |
| Microsoft Certified: Azure Network Engineer Associate | AZ-700 | Jun 2025 | [🔗](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/C1CC44551BE33731?sharingId=AE41C8CE11434D50) |

### 🧩 Microsoft Applied Skills

| Credential | Area |
| :--- | :--- |
| [Configure secure access to your workloads using Azure networking](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/5AC8EB7AB20FD728?sharingId=AE41C8CE11434D50) | Networking |
| [Secure storage for Azure Files and Azure Blob Storage](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/D2AA4099D50AE689?sharingId=AE41C8CE11434D50) | Storage & Security |
| [Deploy and configure Azure Monitor](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/64970AD0DDB23409?sharingId=AE41C8CE11434D50) | Observability |
| [Get started with cloud security and monitoring tasks](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/871FEFDE3CFDE403?sharingId=AE41C8CE11434D50) | Security |
| [Get started with Azure management tasks](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/B80F55F3470B0214?sharingId=AE41C8CE11434D50) | Administration |
| [Get started with identities and access using Microsoft Entra](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/770CE074C6822AA9?sharingId=AE41C8CE11434D50) | Identity |
| [Administer Active Directory Domain Services](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/CBD217E553C8EAAA?sharingId=AE41C8CE11434D50) | Identity |
| [Implement retention, eDiscovery, and Communication Compliance in Microsoft Purview](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/3BAE18873CAA3DD?sharingId=AE41C8CE11434D50) | Compliance |
| [Create and manage automated processes by using Power Automate](https://learn.microsoft.com/api/credentials/share/en-us/Forsythfamous-3964/D0D21E1EBAEEE09F?sharingId=AE41C8CE11434D50) | Automation |

---

# 🤝 Let's Connect

<p align="center">
  <a href="https://github.com/forsythfamous"><img src="https://skillicons.dev/icons?i=github" alt="GitHub" /></a>
  <a href="https://www.linkedin.com/in/forsythazure"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn" /></a>
  <a href="https://dev.to/forsyth_famous_"><img src="https://skillicons.dev/icons?i=devto" alt="dev.to" /></a>
</p>

- **Location:** Poland 🇵🇱
- **Website:** [forsythfamous.pages.dev](https://forsythfamous.pages.dev)
- **Professional Networking:** [LinkedIn](https://www.linkedin.com/in/forsythazure)
- **Technical Writing:** [dev.to/forsyth_famous_](https://dev.to/forsyth_famous_)
- **Credentials:** [Microsoft Learn Profile](https://learn.microsoft.com/en-us/users/forsythfamous-3964/)
- **Open to:** Cloud & DevOps collaboration, technical consulting and new opportunities

---

<p align="center">
  <img src="https://img.shields.io/github/followers/forsythfamous?label=Followers&style=for-the-badge&color=0B3D91&logo=github" alt="GitHub Followers" />
</p>

<p align="center">
  <b>Building reliable cloud infrastructure, one automated step at a time.</b>
</p>

<img width="100%" src="assets/footer.svg" alt="" />
