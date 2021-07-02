# k8s-geekclub
Resources for the NaN-Labs Kuberentes GeekClub!

# How to run

You'll only need docker and docker-compose installed

you need to create 1 files, `.env`

start the cluster by running 

```bash
docker-compose up -d
```

To use the `kubectl` utility inside the compose, change the server url inside `kubeconfig.yaml` to direct to `https://server:6443`

```yaml
# kubeconfig.yaml
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: ==
    server: https://server:6443
  name: default
contexts:
- context:
    cluster: default
    user: default
  name: default
current-context: default
kind: Config
preferences: {}
users:
- name: default
  user:
    password: randmHash
    username: admin
```

