# tech-stouffcapital-elastic

https://medium.com/google-cloud/a-guide-to-deploy-elasticsearch-cluster-on-google-kubernetes-engine-52f67743ee98

docker images: https://www.docker.elastic.co/

## deployment with kubernetes
1. `kelastic-svc.yaml`

### elasticsearch 6.3.2
1. `htpasswd -c auth elastic`
1. `kubectl -n db create secret generic elasticsearch --from-file=auth`
1. `kubectl create -f elastic-elasticsearch.yaml`
1. `kubectl create -f tech-stouffcapital-elasticsearch.yaml`

### kibana 6.3.2
https://eng.fromatob.com/post/2017/02/lets-encrypt-oauth-2-and-kubernetes-ingress/

~~`helm install stable/oauth2-proxy --namespace=utilities -f proxy.yaml --name=elastic-kibana-oauth2`~~

create secret for:
- oauth2-clientId
- oauth2-clientSecret
- oauth2-cookieSecret

1. `kubectl create -f elastic-kibana.yaml`
1. `kubectl create -f tech-stouffcapital-kibana-oauth-proxy.yaml`
