JENKINSFILE SKELETON
---------------------------------------------------------------------------------------------------------

**Se declara sección environment en Jenkinsfile incluyendo en variable PATH la ruta de Maven:**

```

pipeline {
    agent any

    environment {
        PATH = "/usr/lib/jvm/jdk1.8.0_202/bin:/usr/share/maven/bin:${PATH}"
    }

    stages {
        stage ('Show Environment Variables') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    ls -l /usr/share/maven/bin
                    ls -l /usr/lib/jvm/jdk1.8.0_202/bin
                    java -version
                    mvn -version
                ''' 
            }
        }
    }

}

```

-----------------------------------------------------------------------------------------------------------
