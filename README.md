## Operationalize a Machine Learning Microservice API. - Project 4

 This project tests the ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls.

Project Tasks are:

Test your project code using linting
Complete a Dockerfile to containerize this application
Deploy your containerized application using Docker and make a prediction
Improve the log statements in the source code for this application
Configure Kubernetes and create a Kubernetes cluster
Deploy a container using Kubernetes and make a prediction
Upload a complete Github repo with CircleCI to indicate that your code has been tested

---

[![<Udacity>](https://circleci.com/gh/roysrus1/Devops4A.svg?style=svg)](https://app.circleci.com/pipelines/github/roysrus1/Devops4A)

### A. Dependencies
#### A.1. Python
[Download and install the python](https://www.python.org/downloads/). 

#### A.2. Docker Desktop
Required to install Docker Desktop to create containers for individual microservices. Refer the following links for instructions 
* [macOS](https://docs.docker.com/docker-for-mac/install/), 
* [Windows 10 64-bit: Pro, Enterprise, or Education](https://docs.docker.com/docker-for-windows/install/), 
* [Windows  10 64-bit Home](https://docs.docker.com/toolbox/toolbox_install_windows/). 
* You can find installation instructions for other operating systems at:  https://docs.docker.com/install/

#### A.3. Kubernetes 
[Install Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/) - For Linux/macOS

#### A.4. AWS account to access AWS Lambda
You'll need an [AWS account](https://aws.amazon.com/free/?all-free-tier.&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc) to get started with [AWS Lambda](https://aws.amazon.com/lambda/), which is a serverless computing platform on cloud.  

#### A.5. An account with Circle CI
You may sign up on [CircleCI.com](https://circleci.com/signup/) with your GitHub credentials. 

---

### D. Project Instructions

* [Operationalize a Machine Learning Microservice API](https://github.com/udacity/DevOps_Microservices/tree/master/project-ml-microservice-kubernetes): Deploy a containerized, machine learning application using Kubernetes.

To run any project code, you'll have to set up a virtual environment with the project dependencies. All of the following instructions are to be completed via a terminal/command line prompt. 

### E. Create and Activate an Environment

#### E.1. Git and version control
These instructions also assume you have `git` installed for working with Github from a terminal window, but if you do not, you can download that first from this [Github installation page](https://www.atlassian.com/git/tutorials/install-git).

**Now, you're ready to create your local environment!**

1. If you haven't already done so, clone the project repository, and navigate to the main project folder. 
```bash
git clone https://github.com/udacity/DevOps_Microservices.git
cd DevOps_Microservices/project-ml-microservice-kubernetes
```

2. Create (and activate) a new environment, named `.devops` with Python 3. If prompted to proceed with the install `(Proceed [y]/n)` type y.
```bash
python3 -m venv ~/.devops
source ~/.devops/bin/activate
```

At this point your command line should look something like: `(.devops) <User>:project-ml-microservice-kubernetes<user>$`. The `(.devops)` indicates that your environment has been activated, and you can proceed with further package installations.

3. Installing dependencies via project `Makefile`. Many of the project dependencies are listed in the file `requirements.txt`; these can be installed using `pip` commands in the provided `Makefile`. While in your project directory, type the following command to install these dependencies.
```bash
make install
```

Now most of the `.devops` libraries are available to you. There are a couple of other libraries that we'll be using, which can be downloaded as specified, below. 

---

#### E.2. Other Libraries

While you still have your `.devops` environment activated, you will still need to install:
* Docker
* Hadolint
* Kubernetes ([Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/) if you want to run Kubernetes locally)

#### E.3. Docker

You will need to use Docker to build and upload a containerized application. If you already have this installed and created a docker account, you may skip this step.

1. You’ll need to [create a free docker account](https://hub.docker.com/signup), where you’ll choose a unique username and link your email to a docker account. **Your username is your unique docker ID.**

2. To install the latest version of docker, choose the Community Edition (CE) for your operating system, [on docker’s installation site](https://docs.docker.com/v17.12/install/). It is also recommended that you install the latest, **stable** release:

3. After installation, you can verify that you’ve successfully installed docker by printing its version in your terminal: `docker --version`

#### E.4. Run Lint Checks

This project also must pass two lint checks; `hadolint` checks the Dockerfile for errors and `pylint` checks the `app.py` source code for errors.

1. Install `hadolint` following the instructions, [on hadolint's page]( https://github.com/hadolint/hadolint): 

**For Mac:**
```bash
brew install hadolint
```
**For Windows:**
```bash
scoop install hadolint
```
2. In your terminal, type: `make lint` to run lint checks on the project code. If you haven’t changed any code, all requirements should be satisfied, and you should see a printed statement that rates your code (and prints out any additional comments):

```bash
------------------------------------
Your code has been rated at 10.00/10
```

That's about it! When working with kubernetes, you may need to install some other libraries, but these instructions will set you up with an environment that can build and deploy Docker containers.

****************************************************************************************************************************************
Detailed project instructions can be found here:
https://classroom.udacity.com/nanodegrees/nd9991/parts/652b780f-0423-44bb-a7fa-344325b735e1/modules/67fa9db7-42f2-4e6c-a24a-8ae560da4335/lessons/1597126d-6bef-475c-b248-fead1154776a/concepts/3d8293f6-660d-4cf3-ae10-2067364e596b

