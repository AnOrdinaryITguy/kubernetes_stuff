# This is a hobby product testing ECK, please do not use this in production.

## Prerequisites
Make sure you have persistant storage set up before attempting to install this on your kubernetes cluster.
Make sure that your Storage class is configued with the options ```WaitForFirstConsumer``` otherwise stuff breaks...
## Install Instructions
1. Create two privileged namespaces ```elastic-system```(used by ECK operator) and ```elasticstack```(used by eck.yml deploy file).
2. Read the ECK documentation and install the custom resource defintions and the ECK operator with its RBAC rules [ECK documentation](https://www.elastic.co/guide/en/cloud-on-k8s/master/k8s-deploy-eck.html)
3. Deploy with ```kubectl apply -f eck.yaml --namespace=elasticstack```
