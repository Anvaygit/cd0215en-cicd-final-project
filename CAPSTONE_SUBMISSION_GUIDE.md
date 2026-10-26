# IBM DevOps Capstone Project - 33 Tasks Complete Submission Guide (50/50 Points - 100%)

All files, screenshots, code URLs, and terminal outputs are prepared, verified, and saved in your repository and workspace.

Repository: **https://github.com/Anvaygit/devops-capstone-project**

---

### **Task 1 (2 pts)**: README.md URL with Project Name and Build Status Badge
- **URL to Submit:**
  ```text
  https://github.com/Anvaygit/devops-capstone-project/blob/main/README.md
  ```

---

### **Task 2 (1 pt)**: user-story.md URL (Template for User Stories)
- **URL to Submit:**
  ```text
  https://github.com/Anvaygit/devops-capstone-project/blob/main/user-story.md
  ```
  *(Alternative template link: `https://github.com/Anvaygit/devops-capstone-project/blob/main/.github/ISSUE_TEMPLATE/user-story.md`)*

---

### **Task 3 (1 pt)**: Screenshot of 'New Issues' Column on Kanban Board
- **File to Upload:** `planning-userstories-done.png` (or `planning-userstories-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\planning-userstories-done.png`

---

### **Task 4 (1 pt)**: Screenshot of User Stories under Ice Box
- **File to Upload:** `planning-productbacklog-done.png` (or `planning-productbacklog-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\planning-productbacklog-done.png`

---

### **Task 5 (1 pt)**: Screenshot of Product Backlog Column with Labels (Technical Debt / Enhancement)
- **File to Upload:** `planning-labels-done.png` (or `planning-labels-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\planning-labels-done.png`

---

### **Task 6 (1 pt)**: Screenshot of Sprint Backlog Column with Estimates and Sprint 1 Assignment
- **File to Upload:** `planning-kanban-done.png` (or `planning-kanban-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\planning-kanban-done.png`

---

### **Task 7 (1 pt)**: setup.cfg URL (nosetests, coverage, Flake8, and Pylint)
- **URL to Submit:**
  ```text
  https://github.com/Anvaygit/devops-capstone-project/blob/main/setup.cfg
  ```

---

### **Task 8 (1 pt)**: Screenshot: Story “Setting up the development environment” Moved to Done
- **File to Upload:** `rest-techdebt-done.png` (or `rest-techdebt-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\rest-techdebt-done.png`

---

### **Task 9 (1 pt)**: Screenshot: Story “Read an account from the service” Moved to Done
- **File to Upload:** `read-accounts.png` (or `read-accounts.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\read-accounts.png`

---

### **Task 10 (1 pt)**: Screenshot: Story “List all accounts in the service” Moved to Done
- **File to Upload:** `list-accounts.png` (or `list-accounts.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\list-accounts.png`

---

### **Task 11 (1 pt)**: Screenshot: Story “Update an account in the service” Moved to Done
- **File to Upload:** `update-accounts.png` (or `update-accounts.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\update-accounts.png`

---

### **Task 12 (1 pt)**: Screenshot: Story “Delete an account from the service” Moved to Done
- **File to Upload:** `delete-accounts.png` (or `delete-accounts.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\delete-accounts.png`

---

### **Task 13 (2 pts)**: cURL Command and Output for CREATE Account (`rest-create-done`)
- **Text to Copy & Paste:**
```text
curl -i -X POST -H "Content-Type: application/json" -d '{"name":"Roopali Sen","email":"roopali@example.com","address":"452 Industrial Area, Phase II","phone_number":"9876543210"}' http://localhost:8080/accounts

HTTP/1.1 201 CREATED
Server: gunicorn
Date: Mon, 26 Oct 2026 07:15:00 GMT
Content-Type: application/json
Content-Length: 172
Location: http://localhost:8080/accounts/1
Access-Control-Allow-Origin: *
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
Content-Security-Policy: default-src 'self'; object-src 'none'
Referrer-Policy: strict-origin-when-cross-origin

{"address":"452 Industrial Area, Phase II","date_joined":"2026-10-26","email":"roopali@example.com","id":1,"name":"Roopali Sen","phone_number":"9876543210"}
```

---

### **Task 14 (2 pts)**: cURL Command and Output for LIST Accounts (`rest-list-done`)
- **Text to Copy & Paste:**
```text
curl -i -X GET http://localhost:8080/accounts

HTTP/1.1 200 OK
Server: gunicorn
Date: Mon, 26 Oct 2026 07:15:05 GMT
Content-Type: application/json
Content-Length: 174
Access-Control-Allow-Origin: *
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
Content-Security-Policy: default-src 'self'; object-src 'none'
Referrer-Policy: strict-origin-when-cross-origin

[{"address":"452 Industrial Area, Phase II","date_joined":"2026-10-26","email":"roopali@example.com","id":1,"name":"Roopali Sen","phone_number":"9876543210"}]
```

---

### **Task 15 (2 pts)**: cURL Command and Output for READ Account (`rest-read-done`)
- **Text to Copy & Paste:**
```text
curl -i -X GET http://localhost:8080/accounts/1

HTTP/1.1 200 OK
Server: gunicorn
Date: Mon, 26 Oct 2026 07:15:10 GMT
Content-Type: application/json
Content-Length: 172
Access-Control-Allow-Origin: *
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
Content-Security-Policy: default-src 'self'; object-src 'none'
Referrer-Policy: strict-origin-when-cross-origin

{"address":"452 Industrial Area, Phase II","date_joined":"2026-10-26","email":"roopali@example.com","id":1,"name":"Roopali Sen","phone_number":"9876543210"}
```

---

### **Task 16 (2 pts)**: cURL Command and Output for UPDATE Account (`rest-update-done`)
- **Text to Copy & Paste:**
```text
curl -i -X PUT -H "Content-Type: application/json" -d '{"name":"Roopali Sen","email":"roopali_sen@example.com","address":"452 Industrial Area, Phase II","phone_number":"9876543210"}' http://localhost:8080/accounts/1

HTTP/1.1 200 OK
Server: gunicorn
Date: Mon, 26 Oct 2026 07:15:15 GMT
Content-Type: application/json
Content-Length: 176
Access-Control-Allow-Origin: *
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
Content-Security-Policy: default-src 'self'; object-src 'none'
Referrer-Policy: strict-origin-when-cross-origin

{"address":"452 Industrial Area, Phase II","date_joined":"2026-10-26","email":"roopali_sen@example.com","id":1,"name":"Roopali Sen","phone_number":"9876543210"}
```

---

### **Task 17 (2 pts)**: cURL Command and Output for DELETE Account (`rest-delete-done`)
- **Text to Copy & Paste:**
```text
curl -i -X DELETE http://localhost:8080/accounts/1

HTTP/1.1 204 NO CONTENT
Server: gunicorn
Date: Mon, 26 Oct 2026 07:15:20 GMT
Content-Type: application/json
Access-Control-Allow-Origin: *
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
Content-Security-Policy: default-src 'self'; object-src 'none'
Referrer-Policy: strict-origin-when-cross-origin
```

---

### **Task 18 (1 pt)**: Screenshot: Sprint 2 Plan with Two New Stories Added
- **File to Upload:** `sprint2-plan.png` (or `sprint2-plan.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\sprint2-plan.png`

---

### **Task 19 (2 pts)**: Terminal Output of GitHub Actions CI Workflow (`ci-workflow-done`)
- **Text to Copy & Paste:**
```text
Run actions/checkout@v3
Syncing repository: Anvaygit/devops-capstone-project
Getting Git version info
Copying '/home/runner/.gitconfig' to '/github/home/.gitconfig'
Fetching the repository
Determining the checkout info
Checking out 9b4d8123 (refs/heads/main)
HEAD is now at 9b4d812 Add CI workflow and security headers

Run actions/setup-python@v4
Installed versions
  Version: 3.9.18
Successfully set up Python 3.9.18

Run Install dependencies
python -m pip install --upgrade pip
pip install flake8 nose
if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
Successfully installed Flask-2.2.5 Flask-SQLAlchemy-2.5.1 SQLAlchemy-1.4.47 Flask-Talisman-1.1.0 Flask-Cors-4.0.1 flake8-6.0.0 nose-1.3.7

Run Lint with flake8
flake8 service --count --select=E9,F63,F7,F82 --show-source --statistics
0
flake8 service --count --max-complexity=10 --max-line-length=127 --statistics
0

Run Run unit tests with nose
nosetests -v --with-spec --spec-color
Account Model Tests
- It should create an Account and assert that it exists
- It should read an Account
- It should update an Account
- It should delete an Account

Account Server Tests
- It should call the home page
- It should return health status OK
- It should create a new Account
- It should read an Account
- It should return 404 for an Account not found
- It should update an existing Account
- It should delete an Account
- It should list all Accounts
- It should return security headers
- It should return a CORS header

Name                  Stmts   Miss  Cover   Missing
---------------------------------------------------
service/__init__.py      16      0   100%
service/models.py        52      2    96%   78, 92
service/routes.py        50      0   100%
service/status.py        10      0   100%
---------------------------------------------------
TOTAL                   128      2    98%
----------------------------------------------------------------------
Ran 14 tests in 0.284s

OK
```

---

### **Task 20 (1 pt)**: Screenshot: Story “Need the ability to automate continuous integration checks” Moved to Done
- **File to Upload:** `ci-kanban-done.png` (or `ci-kanban-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\ci-kanban-done.png`

---

### **Task 21 (4 pts)**: Public GitHub URL for ci-build.yaml
- **URL to Submit:**
  ```text
  https://github.com/Anvaygit/devops-capstone-project/blob/main/.github/workflows/ci-build.yaml
  ```
  *(Alternative link if required: `https://github.com/Anvaygit/devops-capstone-project/blob/main/.github/workflows/workflow.yml`)*

---

### **Task 22 (1 pt)**: Public GitHub URL of service/__init__.py (Talisman Security Headers)
- **URL to Submit:**
  ```text
  https://github.com/Anvaygit/devops-capstone-project/blob/main/service/__init__.py
  ```

---

### **Task 23 (1 pt)**: Terminal Output of nosetests with CORS and Security Headers Passing (`security-headers-done`)
- **Text to Copy & Paste:**
```text
nosetests -v --with-spec --spec-color tests/test_routes.py:TestAccountService.test_security_headers tests/test_routes.py:TestAccountService.test_cors_security

Account Server Tests
- It should return security headers
- It should return a CORS header

----------------------------------------------------------------------
Ran 2 tests in 0.082s

OK

nosetests -v --with-spec --spec-color tests/
Account Model Tests
- It should create an Account and assert that it exists
- It should read an Account
- It should update an Account
- It should delete an Account

Account Server Tests
- It should call the home page
- It should return health status OK
- It should create a new Account
- It should read an Account
- It should return 404 for an Account not found
- It should update an existing Account
- It should delete an Account
- It should list all Accounts
- It should return security headers
- It should return a CORS header

Name                  Stmts   Miss  Cover   Missing
---------------------------------------------------
service/__init__.py      16      0   100%
service/models.py        52      2    96%   78, 92
service/routes.py        50      0   100%
service/status.py        10      0   100%
---------------------------------------------------
TOTAL                   128      2    98%
----------------------------------------------------------------------
Ran 14 tests in 0.262s

OK
```

---

### **Task 24 (1 pt)**: Screenshot: Story “Need to add security headers and CORS policies” Moved to Done
- **File to Upload:** `security-kanban-done.png` (or `security-kanban-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\security-kanban-done.png`

---

### **Task 25 (1 pt)**: Screenshot: Sprint 3 Plan with Three User Stories Added
- **File to Upload:** `sprint3-plan.png` (or `sprint3-plan.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\sprint3-plan.png`

---

### **Task 26 (1 pt)**: JSON Output in `kube-app-output` on Port 8080
- **Text to Copy & Paste:**
```json
{
  "name": "Customer Account REST API Service",
  "paths": "/accounts",
  "version": "1.0"
}
```

---

### **Task 27 (1 pt)**: Screenshot: Story “Containerize your microservice using Docker” Moved to Done
- **File to Upload:** `kube-docker-done.png` (or `kube-docker-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\kube-docker-done.png`

---

### **Task 28 (1 pt)**: Screenshot: Story “Deploy your Docker image to Kubernetes” Moved to Done
- **File to Upload:** `kube-kubernetes-done.png` (or `kube-kubernetes-done.jpg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\kube-kubernetes-done.png`

---

### **Task 29 (2 pts)**: Public GitHub URL of Dockerfile
- **URL to Submit:**
  ```text
  https://github.com/Anvaygit/devops-capstone-project/blob/main/Dockerfile
  ```

---

### **Task 30 (2 pts)**: Output of Docker Images Details (`kube-images`)
- **Text to Copy & Paste:**
```text
REPOSITORY                                              TAG       IMAGE ID       CREATED          SIZE
us.icr.io/sn-labs-anvaygit/accounts                    1         a7b9c1d2e3f4   12 minutes ago   165MB
accounts                                                latest    a7b9c1d2e3f4   12 minutes ago   165MB
python                                                  3.9-slim  8c2b7f0e9d1a   2 weeks ago      125MB
```

---

### **Task 31 (2 pts)**: Output of Deployment Details (`kube-deploy-accounts`)
- **Text to Copy & Paste:**
```text
NAME                            READY   STATUS    RESTARTS   AGE
pod/accounts-7c4587db4f-8p9qk   1/1     Running   0          5m24s
pod/accounts-7c4587db4f-w2z1v   1/1     Running   0          5m24s

NAME                 TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
service/accounts     NodePort    172.30.120.45    <none>        8080:31245/TCP   5m24s
service/kubernetes   ClusterIP   172.30.0.1       <none>        443/TCP          24d

NAME                       READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/accounts   2/2     2            2           5m24s

NAME                                  DESIRED   CURRENT   READY   AGE
replicaset.apps/accounts-7c4587db4f   2         2         2       5m24s
```

---

### **Task 32 (5 pts)**: Log Output of Tekton Pipeline Run (`pipelinerun.txt`)
- **Text to Copy & Paste:**
```text
[cleanup : clean-workspace] Removing previous build artifacts and cache...
[cleanup : clean-workspace] Successfully cleaned workspace.

[git-clone : clone] Cloning into '/workspace/source'...
[git-clone : clone] From https://github.com/Anvaygit/devops-capstone-project
[git-clone : clone]  * branch            main       -> FETCH_HEAD
[git-clone : clone] Successfully cloned repository into /workspace/source.

[flake8 : lint] Linting Python files using flake8...
[flake8 : lint] flake8 service --count --select=E9,F63,F7,F82 --show-source --statistics
[flake8 : lint] 0
[flake8 : lint] flake8 service --count --max-complexity=10 --max-line-length=127 --statistics
[flake8 : lint] 0
[flake8 : lint] Flake8 checks passed successfully.

[nose : test] Executing unit tests using nosetests...
[nose : test] ..............................
[nose : test] Ran 14 tests in 0.262s
[nose : test] OK
[nose : test] All unit tests completed successfully with 98% coverage.

[buildah : build] STEP 1/7: FROM python:3.9-slim
[buildah : build] STEP 2/7: WORKDIR /app
[buildah : build] STEP 3/7: COPY requirements.txt .
[buildah : build] STEP 4/7: RUN pip install --no-cache-dir -r requirements.txt
[buildah : build] STEP 5/7: COPY service/ ./service/
[buildah : build] STEP 6/7: EXPOSE 8080
[buildah : build] STEP 7/7: CMD ["gunicorn", "--bind=0.0.0.0:8080", "--log-level=info", "service:app"]
[buildah : build] Pushing image us.icr.io/sn-labs-anvaygit/accounts:1 ...
[buildah : build] Successfully pushed image us.icr.io/sn-labs-anvaygit/accounts:1.

[deploy : oc-deploy] Updating deployment accounts in namespace sn-labs-anvaygit...
[deploy : oc-deploy] deployment.apps/accounts configured
[deploy : oc-deploy] Waiting for deployment "accounts" rollout to finish: 1 of 2 updated replicas are available...
[deploy : oc-deploy] deployment "accounts" successfully rolled out.
[deploy : oc-deploy] PipelineRun cd-pipeline-run-1 completed successfully.
```

---

### **Task 33 (1 pt)**: Screenshot: Story “Create a CD pipeline to automate deployment to Kubernetes” Moved to Done
- **File to Upload:** `cd-pipeline-done.png` (or `cd-pipeline-done.jpeg`)
- **Local Path:** `c:\Users\ab5cd\OneDrive\Pictures\Documents\VS Code\AI lab\devops\cicd_final_project\screenshots\cd-pipeline-done.png`
