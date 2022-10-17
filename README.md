# Devops LifeCycle implementation

# In this project i implemented thecomplete devops lifecycle to my old website.

Following are the specification of lifecycle:-

1) Git Workflow has to be implemented
2) Code Build should automatically trigreed once commit is made to main branch or develop branch

   -if commit is made to master branch ,test and push to prod<br>
   -if commit is made to develop branch,just test the product,do not push the prod

3) The code is containerised with the help of Dockerfile.The Dockerfile built every time there is a push to github.

   -The code reside in '/var/www/html'

4) Once the website is build, I designed a test case,which basically checks if the website can be opened or not.if yes test should pass.This test run i headless mode,on the test server.

5) The above task is defined in a Jenkins pipeline ,with the following Jobs

   job1-Building Website<br>
   Job2-Testing Website<br>
   job3-Push to production


<br>
Architecture:-<br>

<br>Created 3 Server on AWS "t2.micro"

Server 1-It consist of jenkins master and nagios installed<br>
Server 2-Testing Server,Jenkins Slave<br>
Server 3-Prod Server,Jenkins Slave

<br>

![Screenshot (79)](https://user-images.githubusercontent.com/62923466/196126799-4ea7b6dc-6acf-4d3b-8f89-a1c354dc5e99.png)<br><br>
![Screenshot (80)](https://user-images.githubusercontent.com/62923466/196126766-5a2e41cb-37e0-42c6-a65f-96c7ad743d64.png)<br><br><br>
![Screenshot (81)](https://user-images.githubusercontent.com/62923466/196126775-c144a732-aecd-49ff-b27b-e8d5df10d7f0.png)<br><br><br>
![Screenshot (83)](https://user-images.githubusercontent.com/62923466/196126780-c1bcda5e-d685-434a-b5a2-6364ff51ef79.png)<br><br><br>
![Screenshot (84)](https://user-images.githubusercontent.com/62923466/196126783-738964d8-6b92-4134-9393-9e9f6f9a0c81.png)<br><br><br>
![Screenshot (85)](https://user-images.githubusercontent.com/62923466/196126788-8d35c900-38f7-405b-8f9f-ccb26d8fd549.png)<br><br><br>
![Screenshot (86)](https://user-images.githubusercontent.com/62923466/196126794-d3192364-f3db-40bd-9282-a17b99ea1895.png)

<br><br>
Checkout the website here:-
https://surajkumar98012.github.io/techsignia/
