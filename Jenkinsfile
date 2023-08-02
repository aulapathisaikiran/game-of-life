pipeline {
	agent { label 'jdk8' }
	stages{
		stage('SourceCode') {
			steps {
			git branch: 'sprint1_devopler', url: 'https://github.com/aulapathisaikiran/game-of-life.git'
}
}

		stage('Bulid the code'){
			steps {
			sh 'mvn clean package'
}
}
		stage('Archiving and Test Results'){
			steps {
			junit '**/surefire-reports/*.xml'
			archiveArtifacts artifacts: '**/*.war', followSymlinks: false
}
}
}
}
