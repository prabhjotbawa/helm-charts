## Installing via helm
Helm must be installed to install to use helm-charts.
### Installing with ingress and cert-manager disabled
To install, run
```commandline
helm repo add my-webapp https://prabhjotbawa.github.io/helm-charts
helm install my-webapp my-webapp/webapp --namespace webapp --create-namespace
```
To upgrade, run
```commandline
helm upgrade my-webapp --reuse-values --namespace webapp
```
To uninstall, run
```commandline
helm uninstall my-webapp --namespace webapp
```
TO check install/upgrade history, run
```commandline
helm history my-webapp --namespace webapp
```

### Installing with ingress and cert-manager enabled
```
helm install my-webapp my-webapp/webapp --namespace webapp --create-namespace --set certManager.enabled=true --set ingress.enabled=true
```
Upgrade and Uninstall commands remain the same as above.