node {
    
    stage('GIT CheckOut') {
    git 'https://github.com/ruchi672/department-micro.git'
  }
  
  stage('Deploy to Kubernetes') {
    sh label: '', script: 'microk8s.kubectl create -f department-service/k8s/deployment.yaml'
  }
   stage('Get all Pods') {
    sh label: '', script: 'kubectl get pods'
  }
}
