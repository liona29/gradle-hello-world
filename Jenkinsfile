pipeline{
    agent{
        label "jenkins-slave"
    }
    stages{
        stage("checkout"){
            steps{
              git 'https://github.com/liona29/gradle-hello-world.git'
            }
        }
        stage("‘build"){
            steps{
              sh "gradle build"
            }
        }        
    }
    post{
        always{
            addBadge icon: 'zine', id: 'zine', link: 'zine', text: 'zine'
        }
        success{
            addBadge icon: 'zinesuccess', id: 'zinesuccess', link: 'zinesuccess', text: 'zinesuccess'
        }
        failure{
            addBadge icon: 'zinefailure', id: 'zinefailure', link: 'zinefailure', text: 'zinefailure'
        }
    }
}
