# Secret ops
```
kubeseal --fetch-cert --controller-name=sealed-secrets-controller --controller-namespace=kube-system > pub-sealed-secrets.pem
```
```
kubeseal --format=yaml --cert=pub-sealed-secrets.pem secret.yaml < secret.yaml > sealed-secret.ya
ml
```
When bootstraping the cluster check that all went well:
```
kubectl get secrets -n=project-namespace
```
