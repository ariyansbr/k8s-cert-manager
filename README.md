# K8s-cert-manager

Cert-manager runs within your Kubernetes cluster as a series of deployment resources. It utilizes CustomResourceDefinitions to configure Certificate Authorities and request certificates.

Install the CustomResourceDefinitions and cert-manager itself :

  Kubernetes 1.15+

``kubectl apply --validate=false -f https://github.com/jetstack/cert-manager/releases/download/v0.14.1/cert-manager.yaml``

After that we should create specific name space for cert-manager 

``kubectl create namespace cert-manager``

Using Helm package manager make installation simple . First of all add the jetstack repo 

``helm repo add jetstack https://charts.jetstack.io``

``helm repo update``

I've installed Helm V3 so : 

``helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --version v0.14.1
``
You should be able to see 3 pods of Cert-manager in Running status . check it : 

``kubectl get pods --namespace cert-manager``

Before you can begin issuing certificates, you must configure at least one Issuer or ClusterIssuer resource in your cluster.

