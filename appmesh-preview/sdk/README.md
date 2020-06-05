# App Mesh Preview SDKs

Some AWS SDKs use a set of JSON models to generate the final SDK. SDKs which allow this include:

* [Go](https://github.com/aws/aws-sdk-go)
* [JavaScript](https://github.com/aws/aws-sdk-js)
* [Ruby](https://github.com/aws/aws-sdk-ruby/)

For these SDKs, you can use the JSON files in this directory to generate an SDK which can be used for the [App Mesh Preview Channel](https://docs.aws.amazon.com/app-mesh/latest/userguide/preview.html).

## Generating an SDK

### Go

Clone the AWS SDK for Go:

```bash
git clone https://github.com/aws/aws-sdk-go.git
cd aws-sdk-go
```

Download the JSON files, replacing the appropriate files in the SDK:

```bash
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/api.json > models/apis/appmesh/2019-01-25/api-2.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/docs.json > models/apis/appmesh/2019-01-25/docs-2.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/examples.json > models/apis/appmesh/2019-01-25/examples-1.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/paginators.json > models/apis/appmesh/2019-01-25/paginators-1.json
```

Generate the SDK:

```bash
make generate
```

### JavaScript

Clone the AWS SDK for JavaScript:

```bash
git clone https://github.com/aws/aws-sdk-js.git
cd aws-sdk-js
```

Download the JSON files, replacing the appropriate files in the SDK:

```bash
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/api.json > apis/appmesh-2019-01-25.min.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/api.normal.json > apis/appmesh-2019-01-25.normal.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/examples.json > apis/appmesh-2019-01-25.examples.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/paginators.json > apis/appmesh-2019-01-25.paginators.json
```

Generate the SDK:

```bash
rake api
```

### Ruby

Clone the AWS SDK for Ruby:

```bash
git clone https://github.com/aws/aws-sdk-ruby.git
cd aws-sdk-ruby
```

Download the JSON files, replacing the appropriate files in the SDK:

```bash
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/api.json > apis/appmesh/2019-01-25/api-2.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/docs.json > apis/appmesh/2019-01-25/docs-2.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/examples.json > apis/appmesh/2019-01-25/examples-1.json
curl -s https://raw.githubusercontent.com/aws/aws-app-mesh-roadmap/master/appmesh-preview/sdk/paginators.json > apis/appmesh/2019-01-25/paginators-1.json
```

Generate the SDK:

```bash
bundle install
rake build
```
