# aws-eb-docker

Using AWS EBS to deploy Node application

See:

https://www.youtube.com/watch?v=RrKRN9zRBWs


Steps:

1. Create a user with role to access ECR

2. Create a ECR repository (Console)

3. Login by CLI:
   
   $ ews configure 
   
4. Login in repository to upload the docker image:

  $ aws ecr get-login-password | docker login --username AWS --password-stdin 765437110318.dkr.ecr.us-east-1.amazonaws.com
   
5. Create your Docker image:

  $ docker build --tag app:1.0 .  
  
6. List your Docker imagem:
  
 $ docker images

7. Tag your docker image:
 
 $ docker tag 599fe8bb1 765437110318.dkr.ecr.us-east-1.amazonaws.com/app
 
8. Push your image to ECR

 $ docker push 765437110318.dkr.ecr.us-east-1.amazonaws.com/app
 






