
#step 1: specify OS
From centos:7

#dir select inside container
WORKDIR '/node-js-app'

#step 2
#download node.js
Run curl -sL https://rpm.nodesource.com/setup_12.x | bash -
Run yum install -y nodejs

#specifying files to copy to tmep docker container (these are the files needed for node.js server to run)

COPY ./package.json  ./server.js /node-js-app/

#install npm dependencies for nodejs server torun (express here acc. to ./package.json file)
run npm install

#open the por needed by the node.js server to run in container
Expose 8000 
#we can change this also for node.js server in server.js file

cmd [ "npm" ,"start"]



