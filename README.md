JENKINS PIPELINE
-----------------------------------------------------------------------------------------------------------

Ejemplos de uso de "declarative pipelines" en Jenkins.

-----------------------------------------------------------------------------------------------------------

Jenkinsfile skeleton:

```

pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building stage is running..."
            }
        }

        stage("Test") {
            steps {
                echo "Testing stage is running..."
            }
        }

        stage("Sonarqube") {
            steps {
                echo "Sonarqube stage is running..."
            }
        }

        stage("Deploy") {
            steps {
                echo "Deploying stage is running..."
            }
        }        
    }

}

```

-----------------------------------------------------------------------------------------------------------