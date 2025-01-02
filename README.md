# Cloud Resume Challenge

This project is a submission for the **Cloud Resume Challenge** using **Microsoft Azure**. It showcases a cloud-hosted resume with a visitor counter, built with a static website for the frontend and an API for the backend.

## Table of Contents

- [Cloud Resume Challenge](#cloud-resume-challenge)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Frontend](#frontend)
  - [Backend](#backend)
  - [Infrastructure](#infrastructure)
  - [CI/CD](#cicd)
  - [Technologies Used](#technologies-used)
  - [Setup Instructions](#setup-instructions)
    - [Frontend](#frontend-1)
    - [Backend](#backend-1)
    - [CI/CD](#cicd-1)
  - [Lessons Learned](#lessons-learned)

---

## Project Overview

The **Cloud Resume Challenge** involves creating a cloud-native resume hosted on Microsoft Azure, with the following features:

- **Static Website:** Resume written in HTML and styled with CSS.
- **Visitor Counter:** A dynamic visitor counter implemented using JavaScript, Azure Functions, and Cosmos DB.
- **Infrastructure as Code (IaC):** Backend infrastructure is defined using Azure Resource Manager (ARM) templates.
- **CI/CD Pipelines:** Automated deployment pipelines for both the frontend and backend.

---

## Frontend

The frontend is a static website containing:

- **HTML:** Contains the structure and content of the resume.
- **CSS:** Adds styling to the resume.
- **JavaScript:** Implements the visitor counter feature.

Deployed as an **Azure Storage Static Website** and secured with **Azure CDN** for HTTPS.

---

## Backend

The backend is an API built with:

- **Azure Functions:** Handles requests for updating and retrieving the visitor count.
- **Cosmos DB (Table API):** Stores the visitor count.

Written in Python and deployed using ARM templates.

---

## Infrastructure

All backend resources, such as the Azure Function and Cosmos DB, are deployed using **Infrastructure as Code (IaC)** via an ARM template. This ensures consistency and repeatability.

---

## CI/CD

Two GitHub repositories are used:

1. **Frontend Repository:** Automatically deploys website updates to Azure Storage when new code is pushed.
2. **Backend Repository:** Runs tests and deploys updates to the Azure Function when changes are made.

**GitHub Actions** is used to implement CI/CD workflows.

---

## Technologies Used

- **Microsoft Azure:**
  - Azure Storage (Static Website Hosting)
  - Azure CDN
  - Azure Cosmos DB (Table API)
  - Azure Functions
- **Programming Languages:**
  - HTML, CSS, JavaScript (Frontend)
  - Python (Backend)
- **Infrastructure as Code:** ARM templates
- **CI/CD:** GitHub Actions

---

## Setup Instructions

### Frontend

1. Clone the repository and navigate to the `frontend` folder:

   ```bash
   git clone https://github.com/<your-username>/cloud-resume.git
   cd frontend
   ```

2. Edit the `index.html` file to customize your resume content and update the visitor counter script if needed.
3. Deploy the website to Azure Storage:

   ```bash
   az storage blob upload-batch --account-name <your-storage-account> --source . --destination '$web'
   ```

4. Set up HTTPS using Azure CDN and map your custom domain to the CDN endpoint.

### Backend

1. Navigate to the `backend` folder:

   ```bash
   git clone https://github.com/<your-username>/cloud-resume.git
   cd frontend
   ```

2. Deploy the ARM template to create the required Azure resources:

   ```bash
   git clone https://github.com/<your-username>/cloud-resume.git
   cd frontend
   ```

3. Install the Python dependencies for the Azure Function:

   ```bash
   git clone https://github.com/<your-username>/cloud-resume.git
   cd frontend
   ```

4. Deploytthe Azure Function:
   ```bash
   git clone https://github.com/<your-username>/cloud-resume.git
   cd frontend
   ```

### CI/CD

1. Set up GitHub Actions for both the frontend and backend repositories.

- For the **frontend**, configure a workflow to automatically upload updated files to Azure Storage and purge the Azure CDN cache.
- For the **backend**, configure a workflow to run Python tests and deploy the Azure Function if the tests pass.

2. Make sure to securely store any Azure credentials or secrets in GitHub Actions secrets.

## Lessons Learned

This section highlights the key takeaways from the project. Some examples include:

- Learned how to use Azure services like Functions, Cosmos DB, and CDN.
- Gained experience with Infrastructure as Code (IaC) using ARM templates.
- Improved skills in implementing CI/CD pipelines with GitHub Actions.
- Enhanced understanding of cloud architecture and cloud-native application development.
