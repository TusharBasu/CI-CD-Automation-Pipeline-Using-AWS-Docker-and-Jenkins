# docker-deployment
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

# Finaly our appliation is deployed on Docker 

![image](https://github.com/TusharBasu/docker-deployment/assets/126240600/cd6472d5-8f27-45c0-bc3e-bfaa70a7d423)





