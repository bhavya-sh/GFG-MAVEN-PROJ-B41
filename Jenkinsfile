pipeline
{
	agent any
		tools
		{
			maven 'MAVEN_HOME'
		}
		stages
		{
			stage('Welcome Stage')
			{
				steps
				{
					echo 'Welcome to Pipeline'
				}
			}
			
			stage('Clean Stage')
			{
				steps
				{
					sh "mvn clean"
				}
			}
			stage('Build Stage')
			{
				steps
				{
					sh "mvn install"
					sh "mv target/gfg-calc.local.jar target/gfg-calc.${BUILD_NUMBER}.jar"
				}
			}
			stage('Build Success')
			{
				steps
				{
					echo 'Build Success'
				}
			}	
			stage('Final Success')
			{
				steps
				{
					echo 'Final Success'
				}
			}	
		}
}
