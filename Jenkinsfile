pipeline {
   agent {
       label "redhat-family"
   }

   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/jafernandez73/blue-pipe-test.git'
            container('centos') {
            // Run Maven on a Unix agent.
                sh "yum --version"
            }
            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }

         post {
            // If Maven was able to run the tests, even if some of the test
            // failed, record the test results and archive the jar file.
            success {

               sh "echo Funciona"
            }
         }
      }
      stage('Test') {
         steps {
            // Get some code from a GitHub repository
            // Run Maven on a Unix agent.
            sh "echo Soy un test"

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }

      }
   }
}
