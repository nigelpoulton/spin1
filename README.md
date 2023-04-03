# Sample spin app

Sample spin app for blog article demo.

Original app and credit: https://github.com/deislabs/containerd-wasm-shims/raw/main/deployments/workloads/workload.yaml

## Files

- `app.yml` contains the the spin app and ingress config
- `rc.yml` contains the RuntimeClass config

The blog post does not use the `rc.yml` file. Instead, it cut & pastes this command block.

```
kubectl apply -f - <<EOF
apiVersion: node.k8s.io/v1
kind: RuntimeClass
metadata:
  name: spin-test
handler: spin
scheduling:
  nodeSelector:
    spin: "yes"
EOF
```
