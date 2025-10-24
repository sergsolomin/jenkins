//Параметры
properties([
    parameters([
        string(name: 'gitSrcUrl', description: 'GIT_URL of project to build'),                                    // Ссылка на гит репозиторий с исходным кодом
        string(name: 'gitSrcBranch', description: 'GIT_BRANCH of project to build'),                              // Ветка в репозитории с исходным кодом
    ])
])

node {
    // Импортируем библиотеки
//    dir('automation'){ checkout scm }
    envs = load "jenkins/env.groovy"
    // Загружаем контекст
//    stash includes: "automation/", name: "automationDir"

    stage('Clean Workspace') {
        sh "echo ${k8sPd15}"
    }   
}


    //Глобальные переменные
    def nexusRepoUrl = "https://nexusRepoUrl/"
//    def clustersPd15 = k8sPd15.split(',').collect{it}

//    def props = readProperties file: 'env.groovy'
//    def props = load 'env.groovy'
//    def k8sPd15 = props.k8sPd15
//    def k8sPd15 = PROPERTY.k8sPd15


//node(){
//
//    environment { 
//        DEBUG_FLAGS = '-g'
//    }
//
//    stage('Clean Workspace') {
//        sh "echo I like to eat ${nexusRepoUrl} eggs"
//        sh "echo ${k8sPd15}"
//        sh "echo ${env.WORKSPACE}"
//    }   
//
//
//}
