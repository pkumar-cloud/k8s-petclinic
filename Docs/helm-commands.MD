# Add stable to helm

```sh
helm repo add stable https://charts.helm.sh/stable

helm repo list

helm repo search <chartname>
helm repo search stable
helm search repo mysql

helm install <releasename> stable/<chartname>
# if present on local:
helm install <releasename> <chartname>
helm list
  
# Pull Helm chart from stable repo in local and create package
helm pull <chartname>
helm pull stable/mysql
  
# Update any default chart artifacts as per needs -> Update Chart.yaml, version field -> Package
helm package <chartname>
helm package mysql

helm uninstall RELEASE_NAME

helm create <chartname>
```
