### This template shows us how to use YAML anchor inside of the helm teplate

#### To test template just use the following command:
```bash
$ helm template --values values.yaml .
---
# Source: ms_name/templates/example.yaml
Greeting: Hello
VaultRoleId: 678903ojksdfgdfyusd
VaultSecretId: df7sd09fsdifis09df9sdf7sd
```     

- Explanation:
For example `&vaultdefaults` function will be used inside for `vault` key as the value inside of the `values.yaml` file. Check `templates/example.yaml` file content it will be more clear.

