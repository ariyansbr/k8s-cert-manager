# k8s-cert-manager

cert-manager runs within your Kubernetes cluster as a series of deployment resources. It utilizes CustomResourceDefinitions to configure Certificate Authorities and request certificates.

Install the CustomResourceDefinitions and cert-manager itself :
# Kubernetes 1.15+

``$ kubectl apply --validate=false -f https://github.com/jetstack/cert-manager/releases/download/v0.14.1/cert-manager.yaml``
