# dockerresume
Implementation:
I have written a dockerfile that will combine the source code for my resume and the httpd apache webserver from official dockerhub images and it will make
a custom image that I can use to deploy my resume on to the cloud.

I ran docker build locally to first see how the resume will appear before I uploaded it onto my public repository in docker hub.

Error:
![Screen Shot 2024-05-17 at 13 54](https://github.com/Sequence-94/dockerresume/assets/53806574/f27cae57-ca36-4ec3-a95d-4346c87ab631)

This is the error I came across when I was attempting to validate my yaml file that will create a laodbalancer which allows me to access my resume. 

Resolution:
The issue kubectl is unable to validate the loadbalancerservice.yaml file because it cannot connect to the Kubernetes API server because I had not yet created my cluster with the below actions on aws.
![Screen Shot 2024-05-17 at 14 25](https://github.com/Sequence-94/dockerresume/assets/53806574/293a0790-705c-41db-8750-ea948a230f06)

Afterwards I was able to see the nodes(compute power) that I created in my cluster and then afterwards I was able to validate and apply my yaml file that would create my loadbalancer service to expose my resume to the internet.
![Screen Shot 2024-05-17 at 14 25 - 2](https://github.com/Sequence-94/dockerresume/assets/53806574/d7e2a3fa-d952-4448-b556-e4b4cb359b10)

As a result I was able to use the external-IP to see my remue:
![Screen Shot 2024-05-17 at 14 31](https://github.com/Sequence-94/dockerresume/assets/53806574/4a899d63-7691-49cf-a0df-7b85458abffd)



