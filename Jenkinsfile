#!usr/bin/env/ groovy

import hudson.model.*
import hudson.EnvVars
import java.net.URL

node {
    stage('GetCode'){
        git 'https://github.com/Anumshr/DevOpsClassCodes.git'
        
    }
    stage('Compile'){
        withMaven(maven:'mymaven'){
        sh 'mvn compile'
        }
    }
    stage('Package'){
        withMaven(maven:'mymaven'){
        sh 'mvn package'
        }
    }
}
