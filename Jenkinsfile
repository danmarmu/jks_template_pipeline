node {

   stage 'Checkout'

   def giturl = 'https://github.com/jglick/simple-maven-project-with-tests.git'
   def gitname = 'Sample Maven Project'


   // Get some code from a GitHub repository
   git url: ${giturl}'https://github.com/jglick/simple-maven-project-with-tests.git'
   //git url: 'https://github.com/jglick/simple-maven-project-with-tests.git'
   
   // Get the maven tool.
   // ** NOTE: This 'M3' maven tool must be configured
   // **       in the global configuration.           
   def mvnHome = tool 'M3'

   // Mark the code build 'stage'....
   stage 'Build'
   // Run the maven build
   sh "${mvnHome}/bin/mvn clean install"
   
   mail bcc: 'daniel.murray@emc.com', \
	body: '${gitname} is built', \
	cc: 'fjdklsa', \
	charset: '', \
	from: 'daniel.murray@emc.com', \
	mimeType: '', \
	replyTo: 'donotreply@emc.com', \
	subject: '${gitname} is built', \
	to: 'daniel.murray@emc.com'


   stage 'Unit Test'
   sh "echo Unit Testing Started"

   stage 'Code Analysis'
   sh "echo Code Analysis Started"

   stage 'Dev Deployment'
   sh "echo Dev Deployment Started"

   stage 'Functional Smoke Test'
   sh "echo Functional Smoke Testing Started"

   stage 'Archive of Release Candidate''
   sh "echo Unit Testing Started"

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
   
