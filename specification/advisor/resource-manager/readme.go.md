## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: advisor
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2017-04
  - tag: package-2017-03
  - tag: package-2016-07-preview
```

### Tag: package-2017-04 and go

These settings apply only when `--tag=package-2017-04 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2017-04' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2017-04-19/$(namespace)
```

### Tag: package-2017-03 and go

These settings apply only when `--tag=package-2017-03 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2017-03' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2017-03-31/$(namespace)
```

### Tag: package-2016-07-preview and go

These settings apply only when `--tag=package-2016-07-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2016-07-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2016-07-12-preview/$(namespace)
```