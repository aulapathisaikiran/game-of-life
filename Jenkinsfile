
pipeline {
	agent { label 'jdk8' }
	stages{
		stage('SourceCode') {
			step {
			git branch: 'sprint1_devopler', url: 'https://github.com/aulapathisaikiran/game-of-life.git'
}
}

		stage('Bulid the code'){
			step {
			sh 'mvn clean package'
}
}
		stage('Archiving and Test Results'){
			step {
			junit '**/surefire-reports/*.xml'
			archiveArtifacts artifacts: '**/*.war', followSymlinks: false
}
}
}
}
