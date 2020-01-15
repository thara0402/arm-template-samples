# Azure Resource Manager Template

## Prepare
```shell-session
$ az account set -s <Subscription ID>
$ az account show
```

## Deploy
```shell-session
$ az group create -n <ResourceGroup Name> -l japaneast
$ az group deployment create -g <ResourceGroup Name> --template-file template.json --parameters parameters.json
```

## Validate
```shell-session
$ az group deployment validate -g <ResourceGroup Name> --template-file template.json --parameters parameters.json
```

## Cleanup
```shell-session
$ az group delete -n <ResourceGroup Name>
```

## Sample
### Virtual Machines
- [複数の仮想マシンを作成する](./vm-copy/template.json)
- [カスタムイメージから複数の仮想マシンを作成する](./vm-copy-custom-image/template.json)
- [Shared Image Gallery から複数の仮想マシンを作成する](./vm-copy-sig/template.json)
