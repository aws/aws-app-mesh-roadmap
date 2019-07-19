# AWS App Mesh Preview CLI Model

## How do I use this?

The easiest way to use this cli model is to load it directly from GitHub, using the following command

```
aws configure add-model \
    --service-name appmesh-preview \
    --service-model https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/service-model.json
```

You can also check out this repository locally, and load the file using the following command

```
aws configure add-model \
    --service-name appmesh-preview \
    --service-model file:///path/to/repo/aws-app-mesh-roadmap/appmesh-preview/service-model.json
```
