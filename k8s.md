# kubectl command snippets


## set-credentials
```
$ kubectl config set-credentials kubeuser/test.cluster.ru --username=test --password='test'
```

## set-cluster
```
$ kubectl config set-cluster test.cluster.ru --insecure-skip-tls-verify=true --server=https://test.cluster.ru
```

## set-context
```
$ kubectl config set-context namespace/test.cluster.ru/kubeuser --user=kubeuser/test.cluster.ru --namespace=namespace --cluster=test.cluster.ru
```

## use-context
```
$ kubectl config use-context namespace/test.cluster.ru/kubeuser
```

## create job from cronjob
```
$ kubectl create job --from=cronjob/crawler catalog-ms-crawler
```
