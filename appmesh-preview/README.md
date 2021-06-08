# AWS App Mesh Preview CLI Model

## How do I use this?

If you are using [AWS CLI v1](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv1.html), you can use the cli model by loading it directly from GitHub, using the following command

```
aws configure add-model \
    --service-name appmesh-preview \
    --service-model https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/main/appmesh-preview/service-model.json
```


If you are using [AWS CLI v2](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html), check out this repository locally, and load the file using the following command

```
aws configure add-model \
    --service-name appmesh-preview \
    --service-model file:///path/to/repo/aws-app-mesh-roadmap/appmesh-preview/service-model.json
```
