stages {
    stage('Build') {
        steps {
            bat 'mvn clean package -DskipTests'
        }
    }

    stage('PMD Check') {
        steps {
            bat 'mvn pmd:pmd'
        }
    }

    stage('Test') {
        steps {
            bat 'mvn test'
        }
    }

    stage('Generate Report') {
        steps {
            bat 'mvn surefire-report:report'
        }
    }

    stage('Generate JavaDoc') {
        steps {
            bat 'mvn javadoc:javadoc'
        }
    }
}
