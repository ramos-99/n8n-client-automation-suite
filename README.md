# 🤖 Client Workflow Automation Suite (Client-Auto-Suite)

## 📌 Project Overview

This project implements a workflow automation system using **n8n** and **Gotenberg** to process incoming client emails. The primary goal is to establish a robust and scalable process to **archive project emails and their attachments** directly into a designated Microsoft OneDrive folder.

## 🚀 Features

* **Email Trigger:** Initiates upon receiving client emails forwarded to a dedicated address.
* **Data Extraction:** Extracts the **Email Subject** (used as the project name or file name).
* **PDF Conversion:** Converts the email body into a **PDF document** (using Gotenberg).
* **Multi-Tenant Archiving:** Uploads the generated PDF and any original attachments to a specified folder in the client's **OneDrive** (via OAuth2 Multi-Tenant setup).

## 🛠️ Requirements

* [**Docker**](https://docs.docker.com/get-docker/) and [**Docker Compose**](https://docs.docker.com/compose/install/) installed.
* **Azure AD App Registration** credentials (Client ID and Secret) for Microsoft Graph (OneDrive) access.

## 💻 Local Setup (Developer)

### 1. Clone the Repository

```bash
git clone [https://github.com/your-username/n8n-client-automation-suite.git](https://github.com/your-username/n8n-client-automation-suite.git)
cd n8n-client-automation-suite
