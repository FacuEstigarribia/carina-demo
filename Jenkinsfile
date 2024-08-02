pipeline {
    agent any
    stages {
        stage ('Clone carina-demo repository') {
            steps {
                git branch: 'main',
                credentialsId: 'git_credentials_faq',
                url: 'https://github.com/FacuEstigarribia/carina-demo.git'
            }
        }

        stage ('Execute API sample suite') {
            steps {
                sh 'mvn clean test -DsuiteFile=src/test/resources/testng_suites/api.xml'
            }
        }
    }
}
