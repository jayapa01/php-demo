pipeline {
        agent { label 'devops' }
        stages{
               stage( " update php server using ansible"){
                 steps{
                        sh "ansible-playbook php-playbook.yaml -e ansible_password=Twright@123# "
                   }
             }
       }
}
