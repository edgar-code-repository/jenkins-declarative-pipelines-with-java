BUILDING JAVA APP
---------------------------------------------------------------------------------------------------------

**Se agregan stages para recuperar una aplicación Java desde un repositorio Git, 
y luego construir y testear dicha aplicación utilizando Maven:**


```

    stage("Cloning Java App from Github") {
        steps {
            echo "Cloning Java App..."
            git 'https://github.com/edgar-code-repository/spring-boot-countries-rest-api'
        }
    }

    stage("Build Java App with Maven") {
        steps {
            echo "Building Java App..."
            sh '''
                mvn -DskipTests clean package
            '''
        }
    }

    stage("Test Java App with Maven") {
        steps {
            echo "Testing Java App..."
            sh '''
                mvn test
            '''
        }           
    }

```

-----------------------------------------------------------------------------------------------------------
