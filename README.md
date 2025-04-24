Build
docker build -t jenkins-custom -f Dockerfile .

# run Jenkins on docker

docker run -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v /usr/local/bin/docker:/usr/local/bin/docker -d --name jenkins-cicd3 -p 8080:8080 -p 50000:50000 jenkins-custom
