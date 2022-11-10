# Istio

## Installing Istio to k8s

Download Istio release:

```sh
curl -L https://istio.io/downloadIstio | sh -

cd istio-1.15.3

# The istioctl client binary in the bin/ directory.
```

Install Istio:

```sh
istioctl install --set profile=demo -y
```

Follow [official instruction](https://istio.io/latest/docs/setup/getting-started/) to deploy sample application:

```sh
kubectl apply -f samples/bookinfo/platform/kube/bookinfo.yaml
```

```sh
kubectl label namespace default istio-injection=enabled
```