@Library('Shared-lib@main')_
pipeline {
       agent any
       stages{
        stage("demo") {
     		steps {
			sayHello 'Vishu'
                       }
                      }
        stage("readfile")
        {
            steps
            {
               
               readFilecode 'C:/Users/883687/Desktop/Hello.csv'
                                       
            }
        }
       }
       post {
        always {
           // emailext body: '${env.BUILD_URL} has result ${currentBuild.result}', subject: 'test email', to: 'vishwajeet751srs@gmail.com'
            mail to: 'vishwajeet751srs@gmail.com',
          subject: "Status of pipeline: ${currentBuild.fullDisplayName}",
          body: "${env.BUILD_URL} has result ${currentBuild.result}"
        }
    }
}
