Follow the steps below to generate a Maven config file for Artifactory access.

1. Go to https://artifactory.octanner.net/webapp/#/home and login with your domain credentials
![Artifactory login page](images/Artifactory Setup 1 - login.png)
2. Click Artifacts
![Artifactory login page](images/Artifactory Setup 2 - artifacts.png)
3. Click Set Me Up
![Artifactory login page](images/Artifactory Setup 3 - set me up.png)
4. Click Insert Credentials
![Artifactory login page](images/Artifactory Setup 4 - insert credentials.png)
5. Enter your domain password
![Artifactory login page](images/Artifactory Setup 5 - type password.png)
6. Click Generate Settings
![Artifactory login page](images/Artifactory Setup 6 - generate settings.png)
7. Download the file
![Artifactory login page](images/Artifactory Setup 7 - download snippet.png)
8. Create the Maven configuration directory
```
  mkdir ~/.m2
```
9. Copy the downloaded file to the Maven configuration directory
```
  cp ~/Downloads/settings.xml ~/.m2/
```
