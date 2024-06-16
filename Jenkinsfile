pipeline {
    agent any

    stages {
        stage('OWASP Dependency-Check Vulnerabilities') {
            steps {
                dependencyCheck additionalArguments: ''' 
                            --format XML --suppression supression.xml
                            ''', odcInstallation: 'Default'
                
                dependencyCheckPublisher pattern: 'dependency-check-report.xml'
            }
        }
    }

    
}