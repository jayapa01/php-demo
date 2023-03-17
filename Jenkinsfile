pipeline {
        agent { label 'devops' }
        stages{
                stage( "Create git tag for commit "){
                 steps{
                        sh """
                          git tag -a v2.0.1  $GIT_COMMIT  -m "creating tag for head"
                          """
                   }
             }
               stage( " update php server using ansible"){
                 steps{
                        sh "ansible-playbook php-playbook.yaml -e ansible_password=Pre@12Red"
                   }
             }
       }
}
