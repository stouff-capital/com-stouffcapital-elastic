# com-stouffcapital-elastic

## deployment with kubernetes
`htpasswd -c auth elastic`

`kubectl create secret generic elastic --from-file=auth`

## kibana

### proxy with oauth2_proxy and github auth
`helm install stable/oauth2-proxy --namespace=default -f proxy.yaml --name=elastic-kibana-oauth2`
