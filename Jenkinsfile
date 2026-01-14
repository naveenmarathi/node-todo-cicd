pipeline {
    agent any

    stages {

        stage("code") {
            steps {
                git url: "https://github.com/naveenmarathi/node-todo-cicd.git", branch: "master"
                echo 'bhaiyya code clone ho gaya'
            }
        }

        stage("build and test") {
            steps {
                sh "docker build -t node-app-test-new ."
                echo 'code build bhi ho gaya'
            }
        }

        stage("scan image") {
            steps {
                echo 'image scanning ho gayi'
            }
        }

        stage("push") {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: "dockerHub",
                        usernameVariable: "dockerHubUser",
                        passwordVariable: "dockerHubPass"
                    )
                ]) {
                    sh "docker login -u ${dockerHubUser} -p ${dockerHubPass}"
                    sh "docker tag node-app-test-new:latest ${dockerHubUser}/node-app-test-new:latest"
                    sh "docker push ${dockerHubUser}/node-app-test-new:latest"
                    echo 'image push ho gaya'
                }
            }
        }

        stage("deploy") {
            steps {
                sh "docker-compose down && docker-compose up -d"
                echo 'deployment ho gayi'
            }
        }
    }
}
