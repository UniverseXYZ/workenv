# workenv# Install aws cli v2 
https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html

# setup aws profile 
```
aws configure
```

# Use a certain AWS profile

```
export AWS_PROFILE=test
```

# Generate kubeconfig 
```
aws eks --region us-east-1 update-kubeconfig --name dev-i-universe-xyz --kubeconfig /home/vadim/.kube/dmob/dmob-kek-dev
```

# Use certain kubeconfig file
```
export KUBECONFIG=/home/vadim/.kube/dmob/dmob-kek-dev
```


# K8s port forward
```
kubectl -n alpha port-forward $(kubectl -n alpha get pods -l component=postgres-proxy -o jsonpath='{.items[0].metadata.name}') 5432
