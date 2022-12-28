pipeline {
  agent {
    docker {image 'crowdar/lippia:3.2.1.1'}
  }
  environment{
    TAG= '@Success'
    TESTTYPE= 'Secuencial'
    LANG= '@EN'
  }
  stages {
      stage('Valores de variables') {
          steps {
            echo "Valores de las variables"
            echo "TAG= $TAG"
            echo "TESTTYPE= $TESTTYPE"
            echo "LANG= $LANG"
            }
      }
      stage('Prueba') {
        steps {
            sh 'ls'
            //sh 'apt-get install -y zip'
            //sh 'mvn test -P$TESTTYPE -Dcrowdar.cucumber.filter="'$TAG'" -Dcrowdar.cucumber.filter.language="'$LANG'"'
        }
      }
  }
}

