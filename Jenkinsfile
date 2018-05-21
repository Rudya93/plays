pipeline {
        agent {label "worker1"}
  
       parameters {
       //string(name: 'quantity', defaultValue: '2', description: 'Quantity of app instances')
        //string(name: 'filter', defaultValue: 'user*', description: 'Filter keyword for security groups')}  
        string(name: 'Branch_Name', defaultValue: 'https://github.com/Rudya93/plays*', description: 'Branch')
        //${params.quantity} ${params.filter}"
       }
    /* environment {
    AWS_BIN = '/home/ec2-user/.local/bin/aws'
    }*/
    stages {
         
           stage ('Users') {
              steps {
             /*   withCredentials([[
            $class: 'AmazonWebServicesCredentialsBinding',
            credentialsId: 'ada1da8c-6363-4223-9c2f-93684d18989a',
            accessKeyVariable: 'AWS_ACCESS_KEY_ID',
            secretKeyVariable: 'AWS_SECRET_ACCESS_KEY'
        ]]) {*/
           // --extra-vars 'Branch_Name=${params.Branch_Name}'
	    sh('/users/script.sh')
	    }}
           
           
           
           stage ('Iptables') {
              steps {
	   //  --extra-vars 'Branch_Name=${params.Branch_Name}'
	      sh('/iptables/script.sh')}}
              }
              }
