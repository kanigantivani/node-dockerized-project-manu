we will create a node js application and we will push the source code into github repository. we will create a repository for nodejs application a we will integrate with jenkins so jenkins will checkout the scm and were we will create a jenkinsfile after pushing the source code into  github repository.  we will integrate with jenkins so jenkins will checkout the scm and were we will create a jenkinsfile inside the jenkins file we will test our code and we will build over code by npm dependencies and then next we will create a docker  image for over node application finally we will push the docker image into a registry like docker hub.
first we reqired ubuntu os ,  t2micro , launch instance, ec2 instance connect through ssh to linux
1.install 
#apt update
#sudo apt install nodejs
#sudo apt install npm

2.once you installed nodejs and npm verify the installation by using this cmds
#node --version
#npm --version
3.go to the official website 
expressjs.com and select getting started option here the straight forward method
4.create a directory 
#mkdir apps
#cd apps
5.then we have to initialized project directory by using 
#npm init
so once you execute these cmd we will get a package.json file package.json file will include all the
dependencies confiuguration of over project
6. install express
#npm install express --save 
#ls
7.create index.js file
#vi index.js
8. we are going to write simple project hello world

const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})

9. run over server index.js
#node index.js
by default port 3000 lets check once browser
we will get hello world so over node application running successfully

10.next we are going test and build this node js application in over local first
we can install mocha
#npm install --save-dev mocha
11.lets verify package.json file
#vi package.json
12.inside the test script  we can execute the mocha 
test"mocha",
build": "echo 'Runnig Build script'"
save
13.we have to create atest directory here
#mkdir test
#cd test
#touch mytest.test.js
cd ..
14 lets verify the 
#npm test
15. lets verify the run cmd
#npm run build
running susccsefully buld script
15. now iam going to push this code into github repository for that first we have to create a repository 
inside the github
16. and we want to initialized git init
#git init
#git status
#git add --all
#git commit -m "first commit"
#git branch -m main
#git remote add origin [past]
#git remote -v
#ssh-keygen -t rsa
#cat ~/.ssh/id_rsa.pub
copy content
17. goto github sellect settings ssh&gpkg key sellect newssh select past
go to linux
#git push -u origin main
#git log
everything push into the github
18. go to the official website 
install jenkins ubuntu os
jenkin dashboard open
19. iam going to create a new pipeline over project
give job name and select pepeline 
we have sucseessfully configured the pipeline go to video integrated with over github
20 .now jenkins will expect a file in over git hub repository
21. we want creat a Docker file for over node application



1. To create ec2 instance take ubuntu os ,t2micro
![1234](https://github.com/user-attachments/assets/5ea4d12f-7c28-4131-8620-a896ac578884)
2. Install nodejs and npm  
 ![2 install nodejs](https://github.com/user-attachments/assets/984bc085-07ee-4abd-86d2-ac0b88a1b192) 
3.  create directory and enter into the directory
 ![3rd create directory and enter into the directory and inialized npm](https://github.com/user-attachments/assets/670f2c15-bb5d-4130-9e30-dc595e620ef7)
4. helloworld file write in index.js
 ![4th helloworld file write in index js](https://github.com/user-attachments/assets/95688a1f-1e2b-47f6-bb56-9b8db7891f8b)
 5. run over server index.js
 ![5th run over index json](https://github.com/user-attachments/assets/3359a3c4-6f14-4742-9ede-f3e49d6d72ee)
6. we will get Helloworld so over node application  running successfully.
 ![we eill get helloworld](https://github.com/user-attachments/assets/dca77d58-2038-466b-8b82-886981838f21)
 7. install mocha
 ![7th install mocha](https://github.com/user-attachments/assets/018c5b4b-5b80-4bc6-be6f-35df137b90fb)
8. lets verify the run cmd and running successfully build
   ![8th lets verify the run cmd and running succesfully build script](https://github.com/user-attachments/assets/8e300cc3-7b10-4c59-839f-c82c9597a5bc)
9. create repo on github
    ![9th create repo in github](https://github.com/user-attachments/assets/d5a3fb76-10a2-4fde-9995-501b3f216d83)
10. everything push into the github
    ![10th everything push into the github](https://github.com/user-attachments/assets/17bfe045-4416-46ed-a7ae-5364cc93c001)
11. pushing into the github
    ![11th push into the git hub repository](https://github.com/user-attachments/assets/cadcd302-4c4a-4c41-a517-64a589b43da5)
12. install jenkins on jenkins server
   ![12 install jenkins on jenkins server](https://github.com/user-attachments/assets/bb86fe74-d1f1-41bc-961c-b0699d10dc3d)
13. jenkins administration
    ![13 jenkins administration](https://github.com/user-attachments/assets/0dcf4647-7f38-4c4a-9bb9-150f738fee3a)
15 create a job on jenkins server
![15 create a job configuration also done](https://github.com/user-attachments/assets/e4af5c65-bd1a-44e7-a5c0-a9cf04ec7349)
16 create a jenkins file in github
 ![16th create jenkins file on github](https://github.com/user-attachments/assets/eca4dff1-2329-45a0-9e8c-8b83d0412644)

 







    
   


      


    
       

    
      

      


 









