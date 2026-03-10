DEVOPS LAB COMMANDS

============================
PROGRAM 1 – BASIC GIT OPERATIONS

git --version

git config --global user.name "yourname"

git config --global user.email "youremail@example.com"

git config --list

mkdir lab1

cd lab1

git init

ls -a

touch index.txt

echo "hello world" > index.txt

cat index.txt

git status

git add index.txt

git add .

git commit -m "version 0.1"

git log

git remote add origin https://github.com/username/repository.git

git branch -M master

git push -u origin master

nano index.txt

git status

git add .

git commit -m "version 0.2"

git push

git log

git clone https://github.com/username/repository.git

ls

cd repository

ls

cat file.txt

============================
PROGRAM 2 – GIT BRANCHING AND MERGING

mkdir lab2

cd lab2

git clone https://github.com/username/devops-test.git

ls

cd devops-test

git branch

git checkout -b feature

git branch

echo "hi bro" > file.txt

git add file.txt

git commit -m "version 0.1"

git checkout main

echo "hi brov" > file.txt

git add .

git commit -m "version 0.2"

git merge feature

nano file.txt

git add file.txt

git commit -m "version 0.3"

git log

git diff main feature

git push origin main

git branch

git pull origin main

ls

cat file.txt

============================
PROGRAM 3 – JENKINS INSTALLATION

sudo apt update

sudo apt install openjdk-21-jdk -y

sudo rm jenkins.war

sudo rm -rf ~/.jenkins

wget https://get.jenkins.io/war-stable/latest/jenkins.war

java -jar jenkins.war --httpPort=8080

sudo apt update

sudo apt install snapd -y

sudo snap install ngrok

ngrok http 8080



pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/LikhithMG/demo1.git'
            }
        }

        stage('Run Script') {
            steps {
                sh 'chmod +x script.sh'
                sh './script.sh'
            }
        }
    }
}





