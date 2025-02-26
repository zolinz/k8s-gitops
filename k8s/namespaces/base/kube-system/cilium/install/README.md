# Cilium

Install the cilium CLI [here](https://docs.cilium.io/en/stable/gettingstarted/k8s-install-default/)

The following installation guide can be followed [here](https://docs.cilium.io/en/v1.9/gettingstarted/kubeproxy-free/#kubeproxy-free)

```bash
kubectl -n kube-system delete ds kube-proxy
```

```bash
helm repo add cilium https://helm.cilium.io/
```

```bash
helm install cilium cilium/cilium \
  --version=1.10.4 \
  --namespace=kube-system \
  --values=k8s/namespaces/base/kube-system/cilium/install/values.yaml
```

Post successful installation of Cilium it's option to run the Cilium network connectivity tests

https://docs.cilium.io/en/v1.10/operations/troubleshooting/#cilium-connectivity-tests
