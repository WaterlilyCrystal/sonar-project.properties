// node {
//   stage('SCM') {
//     checkout scm
//   }
//   stage('SonarQube Analysis') {
//     def scannerHome = tool 'SonarScanner';
//     withSonarQubeEnv() {
//       sh "${scannerHome}/bin/sonar-scanner"
//     }
//   }
// }

node {
 stage('SCM') {
 git branch: 'main', credentialsId: '23581321', url: 'https://github.com/WaterlilyCrystal/sonar-project.properties'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=oop-bee -Dsonar.login=sqa_f930ce38a477bade755ba6f83c69bd850bcc5ee0"
 }
 }
}

