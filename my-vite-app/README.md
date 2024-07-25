# vite + React web application

## Execute the application locally and access it using your browser

Checkout the repo and move to the directory

```
git clone https://github.com/Anideep-Kalia/Pipeline-1.git
cd Pipeline-1/my-vite-app
```
Instal necessary modules to run application

```
Run npm install 
```


For building project
```
npm run build
```
For running the application on local machine at `localhost:5173`
```
npm run dev
```
(or) run it as a Docker container.

** Note: To avoid issues with local setup, Node versions and other dependencies, I would recommend the docker way. **


### The Docker way

Build the Docker Image

```
docker build -t pipeline-1:v1 .
```

```
docker run -d -p 5173:5173 -t pipeline-1:v1
```

Hurray !! Access the application on `http://<ip-address>:5173`


## Next Steps

### Configure a Sonar Server locally

```
apt install unzip
adduser sonarqube
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
unzip *
chmod -R 755 /home/sonarqube/sonarqube-9.4.0.54424
chown -R sonarqube:sonarqube /home/sonarqube/sonarqube-9.4.0.54424
cd sonarqube-9.4.0.54424/bin/linux-x86-64/
./sonar.sh start
```

Hurray !! Now you can access the `SonarQube Server` on `http://<ip-address>:9000` 


