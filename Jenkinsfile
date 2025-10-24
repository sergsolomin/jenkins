//Параметры
properties([
    parameters([
        string(name: 'gitSrcUrl', description: 'GIT_URL of project to build'),                                    // Ссылка на гит репозиторий с исходным кодом
        string(name: 'gitSrcBranch', description: 'GIT_BRANCH of project to build'),                              // Ветка в репозитории с исходным кодом
    ])
])



    //Глобальные переменные
    def nexusRepoUrl = "https://nexusRepoUrl/"


node(){

    environment { 
        DEBUG_FLAGS = '-g'
    }

    dir('automation'){ checkout scm }
    load "automation/config/env.properties"

    def clustersPd15 = k8sPd15.split(',').collect{it}

    stage('Clean Workspace') {
        sh "echo I like to eat ${nexusRepoUrl} eggs"
        sh "echo k8sPd15 ${k8sPd15}"
        sh "echo clustersPd15 ${clustersPd15}"
        sh "echo ${env.WORKSPACE}"
    }   


}
