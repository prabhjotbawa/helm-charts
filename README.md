#  My Community Kubernetes Helm Charts                                      

![Lint Charts](https://github.com/prabhjotbawa/helm-charts/workflows/Lint%20Charts/badge.svg) ![Release Charts](https://github.com/prabhjotbawa/helm-charts/workflows/Release%20Charts/badge.svg) [![Releases downloads](https://img.shields.io/github/downloads/prabhjotbawa/helm-charts/total.svg)](https://github.com/prabhjotbawa/helm-charts/releases)

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