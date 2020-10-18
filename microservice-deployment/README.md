##### Replace Chart name with the current MS_NAME:
```bash
$ cd helm3_atlas && sed -i "s/ms_name/${MS_NAME}/g" Chart.yaml
```

##### Deploy new codes with HELM:

```bash
$ helm upgrade --install --force ${MS_NAME} . -f ${DEPLOY_ENV}.yaml --set image.image_vers=${LAST_TAG},ns_name=${PROJECT_NAME},ms_names.name=${MS_NAME},deploy_env=${DEPLOY_ENV} --kubeconfig $PROD_CREDS --namespace ${PROJECT_NAME}
```
