# decrypt cluster settings with
````
sops -d cluster-secrets.sops.yaml > cluster-secrets.yaml
````

# encrypt cluster settings with
````
sops --encrypt cluster-secrets.yaml > cluster-secrets.sops.yaml 
rm cluster-secrets.yaml
````
