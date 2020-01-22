pipeline
{
 agent any 
 stages{
  stage('Build Application'){
   steps{
   bat 'mvn clean install -nsu -DskipMunitTests'
   }
   }
 
  stage('Deploy Application'){
   steps{
   bat 'mvn package deploy -DmuleDeploy -nsu -DskipMunitTests'
   }
   }
 
  stage('Testing Application'){
   steps{
   bat 'C:\\Users\\smahadevanpillai\\AppData\\Roaming\\npm\\newman run C:\\Users\\smahadevanpillai\\Muleapi-Collection.postman_collection.json -disable-unicode'
   }
   }
  }
}