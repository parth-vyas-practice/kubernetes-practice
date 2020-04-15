Usage Steps:
1. first deploy example and test applications \
`kubectl apply -f example-app.yml` \
`kubectl apply -f test-app.yml` 
2. install nginx ingress controller from following link \
https://github.com/kubernetes/ingress-nginx/ \
https://kubernetes.github.io/ingress-nginx/deploy/#prerequisite-generic-deployment-command \

3. now deploy ingress rules in respected namespace \
`kubectl apply -f example-ingress-rule.yml` \
`kubectl apply -f test-ingress-rule.yml`

4. point domain to ingress controller service and if want to test in local then update /etc/hosts file with domain name and ingress-controller service endpoint

NOTE :
- if want to use ingress-controller then all services type must be ClusterIP
- service, application-pods, and ingress-rule (ingress resource) must be in same namespace
