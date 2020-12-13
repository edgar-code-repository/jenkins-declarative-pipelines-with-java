BUILDING JAVA APP
---------------------------------------------------------------------------------------------------------

**Se agrega stage para recuperar una aplicación Java desde un repositorio Git:** 

```

    stage("Cloning Java App from Github") {
        steps {
            echo "Cloning Java App..."
            git 'https://github.com/edgar-code-repository/spring-boot-countries-rest-api'
        }
    }

```

-----------------------------------------------------------------------------------------------------------

**Se agregan stages para construir y testear la aplicación utilizando Maven:**

```

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

**Se crea pipeline en Jenkins:**

![Screenshot Pipeline](../screenshots/declarative_pipeline_build_java_app.png)

-----------------------------------------------------------------------------------------------------------

**Se configura pipeline para leer Jenkinfile desde un repositorio Git:**

![Screenshot SCM](../screenshots/pipeline_from_scm_build_java_app.png)

-----------------------------------------------------------------------------------------------------------

**Stage view mostrado por Jenkins despues de ejecutar pipeline:**

![Screenshot StageView](../screenshots/pipeline_build_app_stage_view.png)

-----------------------------------------------------------------------------------------------------------