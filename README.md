# Secret Chart

Super simple [OCI](https://helm.sh/blog/storing-charts-in-oci) [Helm](https://helm.sh/) [Chart](https://helm.sh/docs/topics/charts/) to deploy a single [Secret](https://kubernetes.io/docs/concepts/configuration/secret/).

It's signed by [cosign](https://github.com/sigstore/cosign?tab=readme-ov-file#readme) and available through the [GitHub Container Registry](https://github.com/p3lim/secret-chart/pkgs/container/secret-chart%2Fsecret).

See [values.yaml](https://github.com/p3lim/secret-chart/blob/master/charts/secret/values.yaml) for the available options, they mirror the [Secrets v1 specification](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.33/#secret-v1-core).

Example usage with Helm:

```bash
helm install mysecret oci://ghcr.io/p3lim/secret-chart/secret --version 1.0.0 \
  --set stringData.foo='super_secret'
```
