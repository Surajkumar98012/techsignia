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
![Screenshot (79)](https://user-images.githubusercontent.com/62923466/196124860-6b4850e6-d179-4f93-b66f-f4f6f6b18c08.png)

<br><br>
Checkout the website here:-
https://surajkumar98012.github.io/techsignia/
