# Jenkins agent set-up
===============================


### STEPS

#### 1. create two ec2- instances ( ubuntu )
   
   - ubuntu-24 ami
   - t2.micro
   - keypair = agent_key.pem
   - security group = new security-group ----> all traffic ( anywhere )
   - number of instances ---> 2 ( jenkins-master , jenkins-worker )
   - launch instances

#### 2. connect jenkins-master ec2-instance and install jenkins

   - ( follow , how to install jenkins on ubuntu machine )


#### 3. Establish SSh-connectivity between master & worker

##### go to master system and generate ssh-key

`ssh-keygen`

`cd .ssh`

`ls`

`cat id_ed25519.pub`  ---> copy the public key to the `authorized_keys` file on the worker-system.

##### Go to worker-system and execute below commands

`cd .ssh`

`ls`

`cat authorized_keys`

( paste public key )


##### Test connectivity

go to master system , execute below commands

`cd`

`ssh -i id_ed25519 ubuntu@<worker system public dns>`  

(now master can successfully interact with worker)

`exit`

#### 4. Install java on worker system

`sudo apt update`

`sudo apt install fontconfig openjdk-17-jre -y`
