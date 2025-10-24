#!/usr/bin/env groovy
import hudson.model.*

//Параметры
properties([
    parameters([
        string(name: 'gitSrcUrl', description: 'GIT_URL of project to build'),                                    // Ссылка на гит репозиторий с исходным кодом
        string(name: 'gitSrcBranch', description: 'GIT_BRANCH of project to build'),                              // Ветка в репозитории с исходным кодом
    ])
])

node {
    // Импортируем библиотеки
    dir('automation'){ checkout scm }
    workspaceLib = load "automation/env.groovy"
    // Загружаем контекст
//    paramsLib.loadContext('cd', true)
//    stash includes: "automation/", name: "automationDir"
    // Подготавливаем рабочую директорию
//    workspaceLib.prepareWorkspace()
//    envs.setRunMoneEnv()

    stage('Clean Workspace') {
        sh "echo ${k8sPd15}"
    }   
}


    //Глобальные переменные
    def nexusRepoUrl = "https://nexusRepoUrl/"
//    def props = readProperties file: 'env.dev'
//    def props = load 'env.groovy'
//    def k8sPd15 = props.k8sPd15
//    def k8sPd15 = PROPERTY.k8sPd15


node(){

    environment { 
        DEBUG_FLAGS = '-g'
    }

    stage('Clean Workspace') {
        sh "echo I like to eat ${nexusRepoUrl} eggs"
//        sh "echo ${k8sPd15}"
        sh "echo ${env.WORKSPACE}"
    }   

    post {
        always {
            sh "rm -rf ${env.WORKSPACE} || true"
        }
    }

}
