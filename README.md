# Build
docker build -t jenkins-custom -f Dockerfile .

# run Jenkins on docker

docker run -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v /usr/local/bin/docker:/usr/local/bin/docker -d --name jenkins-cicd -p 8080:8080 -p 50000:50000 jenkins-custom

#Open 127.0.0.1:8080 on browser

<img width="1435" alt="image" src="https://github.com/user-attachments/assets/31bdd45b-0c84-4d2b-8cfe-6e986dc93b85" />

#Show initial password reading from file:

docker exec -ti jenkins-cicd cat /var/jenkins_home/secrets/initialAdminPassword

# Copy password to use on Jenkins Login

# Install Suggested plugins

<img width="1317" alt="image" src="https://github.com/user-attachments/assets/973a3836-a0fe-4c1b-9bd3-bafda1bac87f" />

# Wait a few minuts

<img width="1316" alt="image" src="https://github.com/user-attachments/assets/89d9d153-b96c-43b5-8889-c0ab7f803540" />

# Create administrator user

<img width="1308" alt="image" src="https://github.com/user-attachments/assets/92275a76-8221-428e-b9c8-3ce4802e1c0b" />

# We are ready to use Jenkins !!

<img width="1502" alt="image" src="https://github.com/user-attachments/assets/7787c715-143f-4659-ba80-183ba23e4ceb" />
