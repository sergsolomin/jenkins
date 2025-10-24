
//Параметры
properties([
    parameters([
        string(name: 'gitSrcUrl', description: 'GIT_URL of project to build'),                                    // Ссылка на гит репозиторий с исходным кодом
        string(name: 'gitSrcBranch', description: 'GIT_BRANCH of project to build'),                              // Ветка в репозитории с исходным кодом
    ])
])

    //Глобальные переменные
    def nexusRepoUrl = "https://nexusRepoUrl/"
    def props = readProperties file: 'config/env.groovy'


node(){

    stage('Clean Workspace') {
        sh "echo ${k8sPd15}"
        cleanWs()
    }   

}
