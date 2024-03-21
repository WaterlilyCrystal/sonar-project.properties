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
 git branch: 'main', credentialsId: '2357111317', url: 'https://github.com/WaterlilyCrystal/sonar-project.properties'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=oop-bee -
Dsonar.login=sqa_d603f15da221c4f7beac68297e44a02e0983f1f3"
 }
 }
}
