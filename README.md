# DevOps Capstone Project – 01 (Part 1: Client)
## Part 1: Application and Container Building for Client
### 1.2 Client:
#### 1.2.1 Making a separate directory for client to store its related files.

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/6cfabe8a-8f54-4620-a77c-48f259d9f212)

#### 1.2.2 Creating a Dockerfile for client container:

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/c3e121e5-55ff-4ef3-86ec-ed130a494459)

In the above Dockerfile, we have used the official Python image as the base image, installed any necessary packages, copied the client application code, and set the volume mount point at “/clientdata” in the container.

#### 1.2.3 Creating a client application using python:

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/a5e52e86-2129-41f2-9918-0447fab7435d)

Client application that connects to the server, receives a file, and saves it in the “/clientdata” volume/directory.

#### 1.2.4 Creating a “docker-compose.yml” YAML file so that we can define and run the client container using Docker Compose:

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/c1da9531-b033-4f29-b3d5-8b3781b63524)

#### 1.2.5 Running the client container: 
When we run “docker-compose up” command, Docker Compose will build and run the client container with the specified configurations.

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/3fd5b528-4869-440d-bbff-36eddf393216)

We can see that the file has been received and checksum is matched which verifies the received file's integrity.

#### Changing “docker-compose.yml” file in order to make the client application container keep on running:

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/628b359a-967e-4cd8-be19-b2f20615d7cd)

This entrypoint option overrides the internal command option and keeps the container running.

#### Volume created in local machine for client container: 

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/d04941bd-5cfe-4bcb-a1ad-f9c29dc32bd8)

#### Received text file present in both local and container volume (showing that they are shared between host & container):

Local volume:

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/96a073e2-e702-4fff-9942-981028b6a7fa)

Container Volume:

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/6f7cabca-f728-4e8c-8da7-e2d5f9defd7f)

Running Docker Containers (client & server):

![image](https://github.com/nab1999/project1_part1_client/assets/126570628/36641831-434e-403a-b9c1-c883865f7eed)
