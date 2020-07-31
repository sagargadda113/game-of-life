node {
    stage('scm') {
    // some block
        git 'https://github.com/sagargadda113/game-of-life.git'
    }
    stage('Packaging') {
    // some block
        sh label: '', script: 'mvn package'
    }
    stage('Post Build') {
    // some block
        archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false, onlyIfSuccessful: true
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}
