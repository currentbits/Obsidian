<% tp.file.title %>  
**Date:** <% tp.date.now("YYYY-MM-DD HH:mm") %>  
**Kubernetes Cluster:** <% tp.system.prompt("Enter cluster name") %>  
**Namespace:** <% tp.system.prompt("Enter namespace") %>  

## Deployment Overview
**Deployment Name:** <% tp.system.prompt("Enter deployment name") %>  
**Image Version:** <% tp.system.prompt("Enter container image version") %>  
**Replicas:** <% tp.system.prompt("Enter number of replicas") %>  
**Pod Status:** <% tp.system.prompt("Enter pod status (e.g., running, failed)") %>  

## Manifest
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: <% tp.system.prompt("Enter deployment name") %>
  namespace: <% tp.system.prompt("Enter namespace") %>
spec:
  replicas: <% tp.system.prompt("Enter number of replicas") %>
  selector:
    matchLabels:
      app: <% tp.system.prompt("Enter application name") %>
  template:
    metadata:
      labels:
        app: <% tp.system.prompt("Enter application name") %>
    spec:
      containers:
      - name: <% tp.system.prompt("Enter container name") %>
        image: <% tp.system.prompt("Enter container image version") %>
