pipeline {
   agent any
   stages {
      stage('branch-Newmaster2') {
         steps{
            script{
               if (env.GIT_BRANCH == 'origin/Newmaster2'){
                  sleep 120
                  echo "This is Newmaster2......."
               }
            }
         }
      }

      stage('branch-master') {
         when { branch 'origin/Newmaster2' }
         steps{
            echo "when run master......."
         }
      }

      stage('test') {
         steps{
            script{
               if (env.GIT_BRANCH == 'origin/test'){
                  sleep 1
                  echo "run test..."
               }
            }
         }
      }
   }
}