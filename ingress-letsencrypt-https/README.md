Usage Steps:
1. first deploy example applications \
`kubectl apply -f example-app.yml`
2. install nginx ingress controller from following link \
https://github.com/kubernetes/ingress-nginx/ \
https://kubernetes.github.io/ingress-nginx/deploy/#prerequisite-generic-deployment-command \

3. install cert-manager from following link \ 
https://cert-manager.io/docs/installation/kubernetes/ \

4. verify cert-manager by deploying test-resource from installation section

5. deploy issuer or cluster-issuer as per requirement from respective folder
- here normal issuer can only generate ssl certs in same namespace
- cluster issuer can generate ssl certs in any namespace of a cluster

6. deploy ingress-rule with respect to selected issuer folder

NOTE:
- before deploying ingress rule point domain to ingress-controller service endpoint as letsencrypt in this scenario can only generate ssl cert if app you have ownership of domain.
- letsencrypt creates an acme account so email id should be working email-id