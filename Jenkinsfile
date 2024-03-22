node {
    stage('SCM') {
        git branch: 'main', credentialsId: 'github-account', url: 'https://github.com/for-Ely/OOPee.git'
    }
    stage('SonarQube Analysis') {
        def scannerHome = tool 'SonarQube Scanner';
            withSonarQubeEnv() {
                sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=PJ1-OOPee -Dsonar.login=sqa_316d06220643e8838f3fe9a63b651aaad4f2448f"
}
}
}
