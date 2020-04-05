node{
    stage('git checkout'){
        git 'https://github.com/manojr-lab/sample-project-maven'
    }
    stage('Build '){
        def maven= tool name: 'maven-3', type: 'maven'
        sh "${maven}/bin/mvn package"
    }
    stage('Archive artifacts'){
        archiveArtifacts artifacts: 'target/*.war', fingerprint: true, onlyIfSuccessful: true
    }
}