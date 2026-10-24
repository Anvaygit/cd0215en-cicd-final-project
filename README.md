# Customer Accounts Microservice - CI/CD Pipeline

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)
[![CI Workflow](https://github.com/Anvaygit/cd0215en-cicd-final-project/actions/workflows/workflow.yml/badge.svg)](https://github.com/Anvaygit/cd0215en-cicd-final-project/actions)

This repository contains the complete implementation for the **IBM Continuous Integration and Continuous Delivery (CI/CD)** Final Project. It showcases a production-grade CI/CD pipeline for the **Customer Accounts Microservice** using **GitHub Actions**, **Tekton Tasks & Pipelines**, and deployment onto **Red Hat OpenShift**.

---

## Project Overview

- **Project Name:** Customer Accounts Service CI/CD Pipeline
- **Course:** IBM Continuous Integration and Continuous Delivery (CI/CD) - CD0215EN
- **Technologies Used:** Python 3.9, Flask, Flake8, Nose, Tekton Pipelines, Red Hat OpenShift, Kubernetes, Docker

The microservice provides a RESTful API for managing customer accounts:
- `GET /health` - Service health status
- `GET /accounts` - List all customer accounts
- `POST /accounts` - Create a new customer account
- `GET /accounts/{id}` - Retrieve account details
- `PUT /accounts/{id}` - Update account details
- `DELETE /accounts/{id}` - Delete an account

---

## CI/CD Pipeline Architecture

### 1. Continuous Integration with GitHub Actions
- **Trigger:** Automated trigger on all `push` and `pull_request` events to `main` branch.
- **Workflow:** `.github/workflows/workflow.yml`
- **Quality Gates:**
  - Automated dependency setup with Python 3.9
  - Strict code linting using `flake8`
  - Automated unit testing with `nosetests`

### 2. Continuous Delivery with Tekton on Red Hat OpenShift
- **Workspace:** Backed by OpenShift PersistentVolumeClaim (`pvc.yaml`)
- **Tasks (`.tekton/tasks.yml`):**
  1. `cleanup` - Wipes and prepares clean workspace
  2. `git-clone` - Fetches source repository
  3. `flake8` - Enforces style and syntax linting
  4. `nose` - Executes unit test suite
  5. `buildah` - Builds container image using Dockerfile
  6. `openshift-client` - Deploys container image to OpenShift cluster
- **Pipeline (`.tekton/pipeline.yml`):**
  - Sequentially orchestrates the pipeline workflow tasks
  - Manages artifacts and logs across tasks via persistent storage
