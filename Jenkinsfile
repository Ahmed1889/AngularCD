pipeline
{
		agent any
	          stages {
	              stage('pull') {
	                   steps{
	                      script{
	                      checkout([$class: 'GitSCM', branches: [[name: '*/master']],
	                         userRemoteConfigs: [[
	                             credentialsId: '87f0f18f-22ac-4234-a37a-a4c11bebeb69',
	                             url: 'https://github.com/Ahmed1889/AngularCD.git']]])
	                             }
	                             }
	                             }
	              /*stage('Build'){
	              steps{
	              script {
	                      		sh "sudo -S ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml "
	                      }
	                      }
	                      }*/
	                stage('docker'){
	                      steps {
	                      sh "sudo -S ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml "
	                      }
	                }
	          }
}
