node('jdk8') {
        stage('SourceCode') {
                git branch: 'sprint1_devopler', url: 'https://github.com/aulapathisaikiran/game-of-life.git'
        }
        stage('Bulid the code') {
                sh 'mvn clean package'
        }
        stage('Archiving and Test Results') {
                junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
        }

}

