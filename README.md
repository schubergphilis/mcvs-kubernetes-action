# mcvs-kubernetes-action

Mission Critical Vulnerability Scanner (MCVS) Kubernetes Action that consists
of the following steps:

* [yamllint](https://github.com/adrienverge/yamllint)

Use this action to ensure that the Kubernetes deployments are secure and do
not contain any misconfiguration.

## usage

Create a `.github/workflows/kubernetes.yml` file with the following content:

```bash
---
name: Kubernetes
'on': push
jobs:
  mvcs-kubernetes-action:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v4.1.1
      - uses: schubergphilis/mcvs-kubernetes-action@v0.1.0
```

## tools supported

### tools in roadmap
- [kustomize](https://kustomize.io/) | kustomize build . > tmp.yaml | trivy check -f tmp.yaml
- [helm](https://helm.sh/) | 2
- [kpt](https://kpt.dev/)
- [timoni](https://timoni.sh/)
- [kluctl](https://kluctl.io)
- [grafana tanka](https://grafana.com/oss/tanka/)
- [cdk8s](https://cdk8s.io/)
