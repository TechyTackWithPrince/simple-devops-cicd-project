# Simple DevOps Project
<p align="center">
  <img src="https://github.com/devopswithprince/simple-devops-cicd-project/blob/image/_readme_images/project-architecture.png?raw=true" alt="Sublime's custom image"/>
</p>

## This DevOps project can be implemented on laptop ***(no cloud account required)*** consist of following technologies-
- IDE - **VScode, Pycharm**, etc (Recommended but not mandatory)
- Source Code Management as **GitHub**
- CICD tool - **Jenkins**
- Containerization tool - **Docker** (Docker Desktop on Windows/ Mac / Linux)
- **Kubernetes** using docker-dekstop
- CICD tool - **Jenkins**
- IDE - **VScode, Pycharm**, etc (Recommended but not mandatory)


## Git installation
Download and install Git on your local machine - https://git-scm.com/downloads.

Enter below command in terminal(Mac/Linux)/command-prompt(Windows) to clone the project repository-
```bat
git clone https://github.com/devopswithprince/simple-devops-cicd-project.git
```

## IDE installation **(Recommended)**
I recommend any IDE or code editor from below to understand scripts, dockerfile, yaml files, etc in more depth-
- VS code - https://code.visualstudio.com/download
- PyCharm(Community edition) - https://www.jetbrains.com/pycharm/download/
- Sublime - https://www.sublimetext.com/3
- Atom - https://atom.en.softonic.com/download

Click file->Open folder and open the cloned repository here

## Install Docker-Desktop
Download docker-desktop as per your local machines platform - https://www.docker.com/products/docker-desktop/

Windows users might face issue while starting docker-desktop, see below steps-
- Restart docker service in services management console(open run-> enter services.msc)
- Refer below links-
    - https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-containers
    - https://docs.docker.com/desktop/windows/wsl/

I recommend enabling below highlighted options inorder to run the project successfully-

<p align="center">
  <img src="https://github.com/devopswithprince/simple-devops-cicd-project/blob/image/_readme_images/docker-desktop1.png?raw=true" alt="Sublime's custom image"/>
</p>

- Daemon expose option is available in windows docker-desktop. Mac/Linux users can ignore

<p align="center">
  <img src="https://github.com/devopswithprince/simple-devops-cicd-project/blob/image/_readme_images/docker-desktop2.png?raw=true" alt="Sublime's custom image"/>
</p>

- Click on Apply & restart

## Kubernetes configuration
In above step, if you enable Kubernetes, a single node cluster will automatically get created.

Please check if config file is created in below path-
```bat
Windows-
C:\Users\give_your_user_account\.kube
```
```sh
Mac or Linux-
~./kube/
```
## Jenkins setup
Jenkins can be installed locally on your base machine like any other software or can be used as a container.

In my setup, I have installed on base machine for more feasibility.

Jenkins can be downloaded and installed as shown in below links-

- Windows - https://www.jenkins.io/doc/book/installing/windows/
- Mac - https://www.jenkins.io/doc/book/installing/macos/
- Linux - https://www.jenkins.io/doc/book/installing/linux/
- Through Docker as container - https://www.jenkins.io/doc/book/installing/docker/

After Installation, get Administrator password from below-

```powershell
Windows
Get-Content 'C:\Program Files\Jenkins\secrets\initialAdminPassword'
```

```sh
Mac/Linux
cat /var/jenkins_home/secrets/initialAdminPassword
```

```sh
Docker
docker ps

CONTAINER ID   IMAGE                     COMMAND                  CREATED          STATUS          PORTS                                              NAMES
12027cbeebc7   jenkins/jenkins:2.375.1   "/usr/bin/tini -- /u…"   7 seconds ago    Up 6 seconds    0.0.0.0:8080->8080/tcp, 0.0.0.0:50000->50000/tcp   myjenkins

#Take your container id, as shown above and replace with your container id in below command-

docker exec -it 12027cbeebc7 sh -c "cat /var/jenkins_home/secrets/initialAdminPassword"
```
## Application Deployment-
- [Docker-Compose](#docker-compose)

- [Kubernetes](#kubernetes)


### Docker-Compose

- Start Jenkins
- Create pipeline
- Copy & Paste jenkinsfile, make changes wherever necessary
- Trigger pipeline


### Kubernetes
- Start Jenkins
- Create pipeline
- Copy & Paste jenkinsfile, make changes wherever necessary
- Make sure to build images 
- Trigger pipeline


# HAPPY LEARNING!

##### REACHOUT TO ME IF YOU FACE ANY ISSUES.