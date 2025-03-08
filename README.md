# HelmRunner   

This is the repo which have conecept of helm refer Readme

Prerequisites
1) Kubernetes cluster running (local, cloud, or KIND)


 [ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.27.0/kind-linux-amd64

 
 chmod +x ./kind

 
 sudo mv ./kind /usr/local/bin/kind
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
2) kubectl installed and configured.
   curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
   
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"

      echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check
     output: kubectl ok

     sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

     chmod +x kubectl

  mkdir -p ~/.local/bin
  
  mv ./kubectl ~/.local/bin/kubectl
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- 
5) Helm 3 installed. Install Helm with


curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3

chmod 700 get_helm.sh./get_helm.sh

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

go to Artifact.hub and search pakage for Jenkins

helm repo add jenkins https://charts.jenkins.io

helm repo update

now check using

helm repo list

sudo apt-get update


install the jenkins 

helm install jenkins-demo jenkins/jenkins

port-forward
at 8080 
