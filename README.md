# com-stouffcapital-elastic

## deployment with kubernetes
`htpasswd -c auth elastic`

`kubectl create secret generic elastic --from-file=auth`

