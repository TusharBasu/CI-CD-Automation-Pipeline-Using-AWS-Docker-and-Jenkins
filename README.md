# Step-1, Working with Docker and AWS.
## Make a project folder and clone an application to start working.

![Screenshot 2024-06-10 165935](https://github.com/TusharBasu/docker-deployment/assets/126240600/6058e08a-4078-4b24-a24a-e92af0aef3e4)


![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/0e96479c-6a39-4553-b5c2-57bdc9ddb984)

## > Checking whether my server is running on both locally or globally or not.
![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/0b9742d2-4bdf-4975-8a98-6acfc5f4b29d)

> So it's running on both.
> 
*> We can access locally on http://127.0.0.1:8000/*

*> and globally on http://0.0.0.0:8001 (replace 0.0.0.0 with latest public ips)*

## Installing Docker on EC2
![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/9c3d79b0-d0b1-433a-acd2-b9f6386237f9)

*>Create a Docker file to build Image from it.*

*Commands*
````bash
nano Dockerfile
cat Dockerfile
````

![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/d7cd6ada-d710-407b-9c1a-4957cddcc2ff)

*Build image on same directory*
````bash
sudo docker build . -t todo-app
````
https://github.com/TusharBasu/docker-deployment/assets/126240600/9d9261fd-87a3-4c0c-afb9-8f6fc1ad1c79

# >Image build successful with specified image id.

![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/a517ef68-f577-4b57-ab4b-37297d420b89)

# >>Finally our appliation is deployed on Docker<<

![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/cd6472d5-8f27-45c0-bc3e-bfaa70a7d423)

# Step-2, Installation of Jenkins and working with it. 
***Prerequisites***
````bash
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
````

***Now Install Jenkins***

````bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update

sudo apt-get install jenkins

````

***Run commands to strat the jenkins services and check status***

````bash
sudo systemctl start jenkins
````

```bash
sudo systemctl status jenkins
```

![image](https://github.com/TusharBasu/Create-and-Run-CI-CD-Pipeline-Using-AWS-Docker-and-Jenkins/assets/126240600/f7e1bc04-2462-4c53-a429-2e080df37780)


***Edit inbound rule and set 8080 port to access anywhere***
![image](https://github.com/TusharBasu/Create-and-Run-CI-CD-Pipeline-Using-AWS-Docker-and-Jenkins/assets/126240600/378e8227-9d81-41f0-a9e2-089b4cb07181)


# >Now we access jenkins and configure it from anywhere by using public ips

![image](https://github.com/TusharBasu/Create-and-Run-CI-CD-Pipeline-Using-AWS-Docker-and-Jenkins/assets/126240600/839ee0f5-5a70-4aca-b047-939e06301818)

***We can also do same by using docker only***
![image](https://github.com/TusharBasu/Create-and-Run-CI-CD-Pipeline-Using-AWS-Docker-and-Jenkins/assets/126240600/5fb7b2b1-e8d5-4fd6-adf5-5424f79cad81)

***Jenkins Dashboard using AWS***
![image](https://github.com/TusharBasu/CI-CD-Automation-Pipeline-Using-AWS-Docker-and-Jenkins/assets/126240600/4b706d72-c00f-4be7-b5b7-bb8ffbdfd427)



