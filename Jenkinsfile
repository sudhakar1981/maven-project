pipeline{
	 agent any
	 
		stages {
			stage ('Compile Stage') {
				steps{
					withMaven(maven : 'Maven 3.5') {
						bat "mvn clean compile"
						}
					}
				}
			stage ('Testing Stage') {
				steps {
					withMaven(maven : 'Maven 3.5') { 
						bat "mvn test"
					}
				}
			}
			
			stage ('Package Stage') {
				steps {
					withMaven(maven : 'Maven 3.5') {
						bat "mvn package "
					}
				}
			}
			
			stage ('install Stage') {
				steps {
					withMaven(maven : 'Maven 3.5') {
						bat "mvn install"
					}
				}
			}
		}
	}