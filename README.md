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



To create ec2 instance take ubuntu os ,t2micro



