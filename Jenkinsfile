pipeline{
	tools{
		maven 'Maven'
	}
	stages{
		stage('a'){
			steps{
				git branch:'master' url:'https://github.com/rishitabafna/MyMavenJavaApp2.git'
			}
		}
		stage('b'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('c'){
			steps{
				sh 'mvn clean test'
			}
		}
		stage('d'){
			steps{
				sh 'java -jar target//MyMavenJavaApp2-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo 'Build successfully'
		}
		failure{
			echo 'Build failed'
		}
	}
}
