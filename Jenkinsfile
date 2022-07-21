 pipeline
{
    agent{label 'main'}
    tools{maven 'M1'}
    stages
    {
          stage('Checkout')
          {
               steps
               {
                  git branch: 'main', url: 'https://github.com/santoshgit1/SpringPetClinic.git'
               }
         }
         stage('Build')
         {
              steps
              {
                 sh 'mvn compile'
              }
        }
         stage('Test')
        {
             steps
             {
                sh 'mvn test'
              }
         }
         stage('Package')
         {
             steps
             {
                sh 'mvn package'
              }
         }
         stage('Deploy')
         {
             steps
             {
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicScriptedPipeline/target/*.jar'
              }
         }
     }
}
