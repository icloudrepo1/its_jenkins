# Freestyle-project ( using instance ) 👇


# steps :

1. Go to Dashboard
2. Click on New Item
3. Enter an item name = `myproj-1`  ,  Select freestyle method  , Click OK
4. Description = `my freestyle project`
5. Select GitHub project =  `https://github.com/icloudrepo1/jenkins-project-repo.git`
6. Source Code Management =  Git  ---->   Repository URL  =  `https://github.com/icloudrepo1/jenkins-project-repo.git`
7. Credentials  ----->  Click on Add  , Select Jenkins  ----->  Username & PW =  `use your jenkins username and PW`  ,  ID = github-jenkins
8. Click on Build Now
9. `cd /var/lib/jenkins/workspace/myproj-1`

```
sudo apt install nodejs -y
sudo apt install npm -y
sudo npm install
```

### RUN YOUR APPLICATION

```
sudo node app.js
```

Instance-public-ip:8000


===================END====================================

10. Github-jenkins Integration process
  
     - Go to Manage Jenkins
     - Go to Plugins  ------>  Available Plugins  =  Install `GitHub Integration` plugins
     - Select your project and Click on Configure
     - Click on Triggers and Click on `GitHub hook trigger for GITScm polling`
     - Go to Github-repo   ---->  Settings    ----->   Webhooks
     - Payload URL  =  `http://3.111.39.213:8080/github-webhook/`
     - Content type  = Application/json

  ( Now change your code , it automatically deployed )
     - 


===================END====================================



# Freestyle-project ( using container ) 👇


```
sudo apt install docker.io -y
docker --version
```
