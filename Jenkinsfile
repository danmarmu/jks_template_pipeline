#!groovy

node {

   stage 'Checkout'

   def giturl = 'https://github.com/visvv/SimpleMaven.git'
   //def giturl = 'https://github.com/jglick/simple-maven-project-with-tests.git'
   def gitname = 'Sample Maven Project'


   // Get some code from a GitHub repository
   git url: "${giturl}"
   //git url: 'https://github.com/jglick/simple-maven-project-with-tests.git'
   
   // Get the maven tool.
   // ** NOTE: This 'M3' maven tool must be configured
   // **       in the global configuration.           
   def mvnHome = tool 'M3'
   def mvnReturn = "" 
   // Mark the code build 'stage'....
   stage 'Build'
   // Run the maven build
   def mvnReturnText = sh(returnStdout: true, script: "${mvnHome}/bin/mvn clean install").trim()
//      returnStatus: true

   echo " Maven output variable is : ${mvnReturnCode}"
   echo " Maven return variable is : ${mvnReturnText}"
	
//mail from: 'daniel.murray@emc.com', \
//i       to: 'daniel.murray@emc.com', \
//        cc: "daniel.murray@emc.com", \
//        bcc: "daniel.murray@emc.com", \
//        charset: "UTF8", \
//        mimeType: "text/plain", \
//        replyTo: "daniel.murray@emc.com", \
//        subject: "${gitname} is built", \
//	body: "project build error: ${err}"

   mail from: 'daniel.murray@emc.com', \
	to: 'daniel.murray@emc.com', \
	cc: "daniel.murray@emc.com", \
	bcc: "daniel.murray@emc.com", \
	charset: "UTF8", \
	mimeType: "text/plain", \
	replyTo: "daniel.murray@emc.com", \
	subject: "${gitname} is built", \
	body: "${gitname} is built"


   stage 'Unit Test'
   sh "echo Unit Testing Started"

   stage 'Code Analysis'
   sh "echo Code Analysis Started"

   stage 'Dev Deployment'
   sh "echo Dev Deployment Started"

   stage 'Functional Smoke Test'
   sh "echo Functional Smoke Testing Started"

   stage 'Archive of Release Candidate'
   sh "echo Archive of Release Candidatate"

   stage 'Unit Test'
   sh "echo Unit Testing Started"

   stage 'Unit Test'
   sh "echo Unit Testing Started"

   stage 'Unit Test'
   sh "echo Unit Testing Started"

   stage 'Unit Test'
   sh "echo Unit Testing Started"

   stage 'Unit Test'
   sh "echo Unit Testing Started"
}
   
