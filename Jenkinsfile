node {
   def mvnHome
   stage('getscm') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/govi321/spring3-mvc-maven-xml-hello-world.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'Maven'
    }
stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
      echo 'this is build maven artifact'
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
stage ('deploy'){
   echo 'deployment started'
       bat '''copy C:\\Program Files (x86)\\Jenkins\\workspace\\tomcat_deployment\\target\\*.war  C:\\Users\\gujjula'$\\Downloads\\apache-tomcat-8.5.43\\webapps\\'''
   }
}

