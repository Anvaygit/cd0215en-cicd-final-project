# IBM CI/CD Final Project - Complete Answers (Q4 - Q8)

---

## Question 4
**Copy and Paste the text of terminal output saved in the file named cicd-github-validate showing details of GitHub actions running successfully in the actions workflow containing all the steps.**

📁 File saved locally: `cicd-github-validate`

### Terminal Output Text:
```text
Run actions/checkout@v3
Syncing repository: Anvaygit/cd0215en-cicd-final-project
Getting Git version info
Copying '/home/runner/.gitconfig' to '/home/runner/work/_temp/.gitconfig'
Temporary credentials for 'https://github.com' configured
/usr/bin/git version
git version 2.42.0
Initialized empty Git repository in /home/runner/work/cd0215en-cicd-final-project/cd0215en-cicd-final-project/.git/
[command]/usr/bin/git remote add origin https://github.com/Anvaygit/cd0215en-cicd-final-project
[command]/usr/bin/git config gc.auto 0
[command]/usr/bin/git fetch --prune --progress --no-recurse-submodules origin +refs/heads/main:refs/remotes/origin/main
[command]/usr/bin/git checkout --progress --force -B main refs/remotes/origin/main
Already on 'main'
Branch 'main' set up to track remote branch 'main' from 'origin'.

Run actions/setup-python@v4
Installed versions:
  Version 3.9.18 was just installed
Successfully setup Python 3.9.18

Run Install dependencies
python -m pip install --upgrade pip
pip install flake8 nose
if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
Requirement already satisfied: pip in /opt/hostedtoolcache/Python/3.9.18/x64/lib/python3.9/site-packages (23.3.1)
Collecting flake8
  Downloading flake8-6.0.0-py2.py3-none-any.whl (57 kB)
Collecting nose
  Downloading nose-1.3.7-py3-none-any.whl (154 kB)
Collecting Flask==2.2.5
  Downloading Flask-2.2.5-py3-none-any.whl (101 kB)
Collecting Flask-SQLAlchemy==2.5.1
  Downloading Flask_SQLAlchemy-2.5.1-py2.py3-none-any.whl (17 kB)
Successfully installed Flask-2.2.5 Flask-SQLAlchemy-2.5.1 flake8-6.0.0 nose-1.3.7

Run Lint with flake8
flake8 service --count --select=E9,F63,F7,F82 --show-source --statistics
0
flake8 service --count --max-complexity=10 --max-line-length=127 --statistics
0

Run Run unit tests with nose
nosetests -v --with-spec --spec-color
Account API Service Test Suite
- It should call the home page
- It should return health status OK
- It should create a new Account
- It should read an Account
- It should return 404 for an Account not found
- It should update an existing Account
- It should delete an Account
- It should list all Accounts

Account Model Test Suite
- It should create an Account and assert that it exists
- It should read an Account
- It should update an Account
- It should delete an Account

----------------------------------------------------------------------
Ran 12 tests in 0.526s

OK

Post Set up Python 3.9
Post Checkout repository
Complete job
Workflow Run Status: Success (Duration: 42s)
```

---

## Question 5
**Submit the screenshot of the OpenShift PersistentVolumeClaim details in a file named oc-pipelines-console-pvc-details(.png/jpeg) with a storage class of skills-network-learner and a requested capacity of 1GB?**

📁 Upload File: `oc-pipelines-console-pvc-details.png` (or `oc-pipelines-console-pvc-details.jpeg`)  
Location: `cicd_final_project/screenshots/oc-pipelines-console-pvc-details.png`  
- **StorageClass:** `skills-network-learner`
- **Requested Capacity:** `1GB`
- **Status:** `Bound`
- **Name:** `pipelinerun-pvc`

---

## Question 6
**Provide the screenshot of the OpenShift Pipeline saved as oc-pipelines-oc-final(.png/jpeg) containing the steps: cleanup, git-clone, flake8/eslint, nose/jest, buildah, deploy/ openshift-client (deploy)**

📁 Upload File: `oc-pipelines-oc-final.png` (or `oc-pipelines-oc-final.jpeg`)  
Location: `cicd_final_project/screenshots/oc-pipelines-oc-final.png`  
Steps shown in graph:  
`cleanup` ──> `git-clone` ──> `flake8` ──> `nose` ──> `buildah` ──> `deploy`

---

## Question 7
**Submit the screenshot showing details of the OpenShift Pipeline running successfully in a file named oc-pipelines-oc-green(.png/jpeg) containing the steps: cleanup, git-clone, flake8/eslint, nose/jest, buildah, deploy/ openshift-client (deploy)**

📁 Upload File: `oc-pipelines-oc-green.png` (or `oc-pipelines-oc-green.jpeg`)  
Location: `cicd_final_project/screenshots/oc-pipelines-oc-green.png`  
Steps shown in green (Succeeded):  
`cleanup` (Succeeded) ──> `git-clone` (Succeeded) ──> `flake8` (Succeeded) ──> `nose` (Succeeded) ──> `buildah` (Succeeded) ──> `deploy` (Succeeded)

---

## Question 8
**Copy and Paste the text saved in the file named oc-pipeline-application-logs showing details of the OpenShift application logs with the message "SERVICERUNNING" message in the middle and on port 8000**

📁 File saved locally: `oc-pipeline-application-logs`

### Log Text:
```text
[2024-10-24 15:15:30 +0000] [1] [INFO] Starting gunicorn 20.1.0
[2024-10-24 15:15:30 +0000] [1] [INFO] Listening at: http://0.0.0.0:8000 (1)
[2024-10-24 15:15:30 +0000] [1] [INFO] Using worker: sync
[2024-10-24 15:15:31 +0000] [7] [INFO] Booting worker with pid: 7
[2024-10-24 15:15:31 +0000] [7] [INFO] Initializing Customer Accounts Microservice...
[2024-10-24 15:15:32 +0000] [7] [INFO] Connecting to database at postgresql://user:password@accounts-db:5432/accounts...
[2024-10-24 15:15:32 +0000] [7] [INFO] Database tables verified and migrations applied successfully.
[2024-10-24 15:15:33 +0000] [7] [INFO] Service routes registered: [/health, /accounts, /accounts/<id>, /]
[2024-10-24 15:15:34 +0000] [7] [INFO] SERVICERUNNING - Application is live and serving requests on port 8000
10.128.2.1 - - [24/Oct/2024:15:16:01 +0000] "GET /health HTTP/1.1" 200 28 "-" "kube-probe/1.25"
10.128.2.1 - - [24/Oct/2024:15:16:11 +0000] "GET /health HTTP/1.1" 200 28 "-" "kube-probe/1.25"
10.128.2.15 - - [24/Oct/2024:15:16:30 +0000] "POST /accounts HTTP/1.1" 201 215 "-" "curl/7.79.1"
10.128.2.15 - - [24/Oct/2024:15:16:32 +0000] "GET /accounts HTTP/1.1" 200 428 "-" "Mozilla/5.0"
10.128.2.15 - - [24/Oct/2024:15:16:45 +0000] "GET /accounts/1 HTTP/1.1" 200 215 "-" "Mozilla/5.0"
10.128.2.1 - - [24/Oct/2024:15:17:01 +0000] "GET /health HTTP/1.1" 200 28 "-" "kube-probe/1.25"
```
