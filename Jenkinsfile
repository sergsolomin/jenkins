
//Параметры
properties([
    parameters([
        string(name: 'gitSrcUrl', description: 'GIT_URL of project to build'),                                    // Ссылка на гит репозиторий с исходным кодом
        string(name: 'gitSrcBranch', description: 'GIT_BRANCH of project to build'),                              // Ветка в репозитории с исходным кодом
    ])
])

    //Глобальные переменные
    def nexusRepoUrl = "https://nexusRepoUrl/"
    def props = readProperties file: 'env.groovy'
    def k8sPd15 = props.k8sPd15

environment {
    FAVOURITE_FILM = 'The Goonies'
}

node(){

    stage('Clean Workspace') {
        sh "echo I like to eat ${FAVOURITE_EGG_TYPE} eggs"
        sh "echo ${k8sPd15}"
        cleanWs()
    }   

}
