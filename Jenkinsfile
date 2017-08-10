#!/usr/bin/env groovy
node {
	stage('Git Clone'){
		git credentialsId: 'ID1', url: 'git@github.com:rezap/gildedrose.git'
	}
	stage('Build'){
	sh 'docker run -i --rm --name my-maven-project -v "$PWD":/usr/src/mymaven -w /usr/src/mymaven maven:3-jdk-8 mvn install'
	}
}
