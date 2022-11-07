# Installing flux

## Downloading fluxctl

Download latest fluxctl binary from https://github.com/fluxcd/flux/releases

## Deploying flux to k8s cluster

Create namespace for flux:

```sh
kubectl create ns flux
```

Replace your own git user/email/repo-url below:

```sh
fluxctl install \
--git-user=ruijzhan \
--git-email=qiudog825@gmail.com \
--git-url=git@github.com:ruijzhan/scripts \
--namespace=flux | kubectl apply -f -
```
