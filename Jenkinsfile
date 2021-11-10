pipeline
{
		agent any
	          stages {
	              stage('pull') {
	                   steps{
	                      script{
	                      checkout([$class: 'GitSCM', branches: [[name: '*/master']],
	                         userRemoteConfigs: [[
	                             credentialsId: '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',
	                             url: 'https://github.com/Ahmed1889/AngularCD.git']]])
	                             }
	                             }
	                             }
	          }
}
