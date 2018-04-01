pipeline{
	 agent any
	 
		stages {
			stage ('Compile Stage') {
				steps{
					withmaven(maven : 'MAVEN_HOME') {
						bat 'mvn clean compile'
						}
					}
				}
			stage ('Testing Stage') {
				steps {
					withmaven(maven : 'MAVEN_HOME') { 
						bat 'mvn test'
					}
				}
			}
			
			stage ('Deployment Stage') {
				steps {
					withmaven(maven : 'MAVEN_HOME') {
						bat 'mvn deploy'
					}
				}
			}
		}
	}