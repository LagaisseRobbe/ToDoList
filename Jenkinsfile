node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop Todolist'
            sh 'docker rm Todolist'
        }
    }
    stage('Build') {
        build 'BuildTodoList'
    }
    stage('Results') {
        build 'TestTodoList'
    }
}