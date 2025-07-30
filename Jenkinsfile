// Tout pipeline déclaratif commence par ce bloc 'pipeline'
    pipeline {
        // 'agent any' signifie que ce pipeline peut s'exécuter
        // sur n'importe quel agent Jenkins disponible.
        agent any

        // 'stages' contient toutes les étapes séquentielles de notre pipeline.
        stages {
            
            // Premier stage : compilation du code
            stage('Build') {
                steps {
                    echo 'Building the application...'
                    // On exécute une commande shell pour lancer la compilation Maven.
                    // './mvnw' est le Maven Wrapper, il évite d'avoir à installer
                    // Maven sur l'agent Jenkins.
                    sh './mvnw compile'
                }
            }
            
            // Second stage : exécution des tests unitaires
            stage('Test') {
                steps {
                    echo 'Running tests...'
                    sh './mvnw test'
                }
            }
        }
    }