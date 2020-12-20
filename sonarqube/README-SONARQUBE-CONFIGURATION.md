SONARQUBE AND JENKINS CONFIGURATION
---------------------------------------------------------------------------------------------------------

**Se genera token dentro de Sonarqube para ser utilizado desde Jenkins:**

![Screenshot Token](../screenshots/sonarqube_generated_token.png)

-----------------------------------------------------------------------------------------------------------

**Se instala plugin SonarQube Scanner en Jenkins (Manage Jenkins -> Manage Plugins):**

![Screenshot SonarQubePlugin](../screenshots/SonarQubeScannerInJenkins.png)

-----------------------------------------------------------------------------------------------------------

**Se crea credencial tipo secret text para configurar token creado en Sonarqube** 

**(Manage Jenkins -> Manage Credentials)**

![Screenshot SecretText](../screenshots/secret-text-for-sonarqube.png)

-----------------------------------------------------------------------------------------------------------

**Se configura servidor Sonarqube en Jenkins (Manage Jenkins -> Configure System):**

![Screenshot ConfigureSonarqube](../screenshots/sonarqube-configuration-in-jenkins.png)

-----------------------------------------------------------------------------------------------------------

**Se configura SonarQube Scanner en Jenkins (Manage Jenkins -> Global Tool Configuration):**

![Screenshot Scanner](../screenshots/scanner-configuration-in-jenkins.png)

-----------------------------------------------------------------------------------------------------------
