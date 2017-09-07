#!/usr/bin/env groovy
import hudson.ProxyConfiguration

node {
    stage('Checkout') {
        git credentialsId: 'github-kkyb123-credentials',
                url: 'https://github.com/kkyb123/hellogroovy.git'
    }

    stage('Api Call') {
        if (ProxyConfiguration.load() == null){
            echo 'No proxy configuration'
        }else {
           httpRequest 'https://www.google.cm'
        }
    }
}
