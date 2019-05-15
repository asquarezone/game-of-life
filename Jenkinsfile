node("ANSIBLE") {
		stage('git') {
    git branch: 'Dev', credentialsId: 'mvn', url: 'https://github.com/LAKSHMIJODI/game-of-life'
	}
	stage('maven'){
	sh label: '', script: 'mvn package'
	}
	stage('tree'){
	sh label: '', script: 'sudo apt-get install tree'
	}
	stage('artifacts'){
	archive '/target*.jar'
	}
}



