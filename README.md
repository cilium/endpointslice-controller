# EndpointSlice Controller

This repository is a fork of k8s endpointslice controller pkg available [here](https://github.com/kubernetes/kubernetes/blob/v1.29.0/pkg/controller/endpointslice)

This fork was created to avoid importing k8s.io/kubernetes into projects.

The diff between the upstream and this fork should be minimal. In case this
repository needs to be updated, the following commands should be performed:

```bash
tag="v1.29.3"
url="https://raw.githubusercontent.com/kubernetes/kubernetes/${tag}"

curl "${url}/pkg/controller/endpointslice/endpointslice_controller.go" > endpointslice/endpointslice_controller.go
curl "${url}/pkg/controller/endpointslice/endpointslice_controller_test.go" > endpointslice/endpointslice_controller_test.go
curl "${url}/pkg/controller/endpointslice/OWNERS" > endpointslice/OWNERS

curl "${url}/pkg/controller/endpointslice/config/doc.go" > endpointslice/config/doc.go
curl "${url}/pkg/controller/endpointslice/config/types.go" > endpointslice/config/types.go
curl "${url}/pkg/controller/endpointslice/config/zz_generated.deepcopy.go" > endpointslice/config/zz_generated.deepcopy.go

curl "${url}/pkg/controller/util/endpointslice/errors.go" > util/endpointslice/errors.go
curl "${url}/pkg/controller/util/endpointslice/OWNERS" > util/endpointslice/OWNERS
```

And manually check if there are no major differences between the upstream and
the fork.
