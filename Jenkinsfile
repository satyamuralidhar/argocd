pipeline {
    agent any 
    stages { 
         stage("scm using git"){
            steps {
                sh"git --version && sleep 2"
                sh"git remote prune origin --dry-run"
                //sh '''git clone https://github.com/satyamuralidhar/argocd.git'''
                git url: 'https://github.com/satyamuralidhar/argocd.git'
            }
        }
        stage("k8s argocd"){
            steps {
                sh '''kubectl apply -f argocd/argocd.yaml -n satya'''
            }
        }
    }
}
