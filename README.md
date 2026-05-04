# reusable-workflows

```bash
helm template . --set "ingress.host=dummy.owner.duckdns.org" --set "useConfigFile=false" | kubeconform \
  -summary \
  -strict \
  -schema-location default \
  -schema-location 'https://raw.githubusercontent.com/datreeio/CRDs-catalog/main/{{.Group}}/{{.ResourceKind}}_{{.ResourceAPIVersion}}.json'
```
