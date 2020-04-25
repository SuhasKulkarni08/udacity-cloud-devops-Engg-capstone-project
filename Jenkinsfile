pipeline {
	agent any
	stages {
		

		stage('Create conf file cluster') {
			steps {
				withAWS(region:'ap-south-1', credentials:'capstone_aws_credentials') {
					sh '''
						~/.local/bin/aws eks --region ap-south-1 update-kubeconfig --name capstonecluster
					'''
				}
			}
		}

	}
}
