pipeline {
 agent {label 'ANSIBLE'}
  stages {
     stage ("vcs") {
        steps {
          git url: "https://github.com/subrAt5238/ansible-jenkins.git",
          branch: "master"
        }
    }
     stage ("ansible") {
        steps ("playbook") {
          sh "ansible -i hosts -m ping all"
          sh "ansible-playbook -i hosts wildfly.yaml"
        }
    }
  }
}