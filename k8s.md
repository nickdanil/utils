# kubectl command snippets


## set-credentials
```
$ kubectl config set-credentials kubeuser/test.cluster.ru --username=test --password='test'
$ kubectl config set-credentials user_dev --token=eyJhbGciOiJSUzI1NiIsImtpZCI6IkVmbmdlY1h5TjFMSTdLSVdOd1pvNEFiRnpfWmJfeVhfcWVQaFpLUlBlZTQifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJkMC1kYm91LWdlbmVyYWwiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlY3JldC5uYW1lIjoiZGJvdS1yZWFkLXNhLXRva2VuIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6ImRib3UtcmVhZC1zYSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VydmljZS1hY2NvdW50LnVpZCI6IjY2MGRlMzI1LTU3NDYtNDBhNC1hMjNiLTUyODY2NmViODMxYyIsInN1YiI6InN5c3RlbTpzZXJ2aWNlYWNjb3VudDpkMC1kYm91LWdlbmVyYWw6ZGJvdS1yZWFkLXNhIn0.LwYm_bss3MnzCcWUf1Dyr4SNRF1gHQjfxEUPAZXnpKfO_gfuAZ8x-HNSrekMY9rE_7P3oZ3WLOPACvXJmEpmIsmh50VPl1dnrLtp90CMeOvW66AwKyjMY-kf_9z4vQyM_1tiONMI3Fr0Q2euUgOM6MTsG-br-YO7-p8oU2XOA64rxYdtUtNmwQm1Ayuc9NyuqU4F9eAtk58TZDHnv4C9wU_Vhb0-rOSTFipLFDLkgcPJgmCHxmIqlYNj64dA3Uw5pq5NLFOc9KgP873q5R4MjfLEq7bYYctIyCcxLWztLEK4G68WW1d_khYD55HIGx3Z7CGRGQ--ot95zy88vjYa4w
```

## set-cluster
```
$ kubectl config set-cluster test.cluster.ru --insecure-skip-tls-verify=true --server=https://test.cluster.ru
$ kubectl config set-cluster dev --insecure-skip-tls-verify=true --server=https://api.d0-k8s-01.dev.su:6443
```

## set-context
```
$ kubectl config set-context cluster_dev_dbou --user=user_dev --namespace=d0-dbou-general --cluster=cluster_dev
```

## use-context
```
$ kubectl config use-context dev
```

## create job from cronjob
```
$ kubectl create job --from=cronjob/crawler catalog-ms-crawler
```

## k8s fast commands
``` 
kubectl delete pod <pod-name>-57bc8dcb9d-ld7sh --grace-period=0 --force --namespace <namespace> --kubeconfig=./Documents/k8s/test.txt

kubectl logs <pod-name>-64898ddccb-9ml5x --namespace <namespace> --kubeconfig=~/Documents/k8s/test.txt

kubectl cp <namespace>/<pod-name>-84bb556c59-n5x4d:/usr/lib/jvm/jdk-11.0.17-bellsoft-x86_64/lib/security/caserts /Users/User/Downloads/caserts-pod-prod --namespace <namespace> --kubeconfig=/Users/User/Documents/k8s/prod.txt
```