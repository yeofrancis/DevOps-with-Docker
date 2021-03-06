# DevOps-with-Docker

#### Containerization versus virtualization
A virtual machine emulates a computer architecture and provides the functionality of a physical computer. We can achieve complete isolation of applications if each of them is delivered and run as a separate virtual machine image.

The concept of virtualization:

![image](https://user-images.githubusercontent.com/82499575/145829539-4d4e45c5-b9b2-4510-9209-f53dec65eec8.png)

Virtualization, however, has three significant drawbacks:
  - Low performance: The virtual machine emulates the whole computer architecture to run the guest operating system, so there is a significant overhead associated with each operation.
  - High resource consumption: Emulation requires a lot of resources and has to be done separately for each application. This is why, on a standard desktop machine, only a few applications can be run simultaneously.
  - Large image size: Each application is delivered with a full operating system, so the deployment on a server implies sending and storing a large amount of data.
 
 The concept of containerization presents:
 
 ![image](https://user-images.githubusercontent.com/82499575/145830063-41470365-479b-4453-af65-6982e19759c3.png)

Each application is delivered together with its dependencies, but, without the operating system. Applications interface directly with the host operating system, so there is no additional layer of the guest operating system. It results in better performance and no waste of resources.

# Continious Integration / Continious Delivery with Docker

The Developer's inner loop and outer loop shown below. To this, we want the inner loop and the outer loop to be mirrored as much as possible.

![image](https://user-images.githubusercontent.com/82499575/147209690-349fb938-7daf-4dce-a736-accb37a4aed3.png)

#### Running Docker Container 
```
docker container run nginx:alpine
```
#### Publish the container
run in the background and publishes port 80 inside the container to port 80 on the host
```
$ docker container run --detach --publish 80:80 nginx:alpine
```
browse to  browse to  browse to http://localhost and see the Nginx welcome page
 
![image](https://user-images.githubusercontent.com/82499575/147880608-7255e51b-5e9b-458f-ace5-752742c59563.png)

