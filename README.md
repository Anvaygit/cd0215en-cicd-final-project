# DevOps Capstone Project

[![Build Status](https://github.com/Anvaygit/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/Anvaygit/devops-capstone-project/actions)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://github.com/Anvaygit/devops-capstone-project/actions)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

This repository contains the complete implementation for the **DevOps Capstone Project**. It showcases a production-grade Customer Accounts Microservice with **RESTful APIs**, automated testing with **Nose** and **Coverage**, security headers via **Talisman** and **CORS**, automated Continuous Integration via **GitHub Actions**, containerization with **Docker**, and automated deployment on **Kubernetes / Red Hat OpenShift** via **Tekton Pipelines**.

---

## Project Overview

- **Project Name:** DevOps Capstone Project
- **Microservice:** Customer Accounts Service
- **Technologies Used:** Python 3.9, Flask, Flake8, Nose, Tekton Pipelines, Red Hat OpenShift, Kubernetes, Docker

The microservice provides a RESTful API for managing customer accounts:
- `GET /health` - Service health status
- `GET /accounts` - List all customer accounts
- `POST /accounts` - Create a new customer account
- `GET /accounts/{id}` - Retrieve account details
- `PUT /accounts/{id}` - Update account details
- `DELETE /accounts` - Delete an account
- `DELETE /accounts/{id}` - Delete an account by id

---

## CI/CD Pipeline Architecture

### 1. Continuous Integration with GitHub Actions
- **Trigger:** Automated trigger on all `push` and `pull_request` events to `main` branch.
- **Workflow:** `.github/workflows/ci-build.yaml`
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
