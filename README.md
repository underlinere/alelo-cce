## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_huaweicloud"></a> [huaweicloud](#requirement\_huaweicloud) | 1.31.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_huaweicloud"></a> [huaweicloud](#provider\_huaweicloud) | 1.31.0 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [huaweicloud_cce_addon.ingress](https://registry.terraform.io/providers/huaweicloud/huaweicloud/1.31.0/docs/resources/cce_addon) | resource |
| [huaweicloud_cce_addon.metrics](https://registry.terraform.io/providers/huaweicloud/huaweicloud/1.31.0/docs/resources/cce_addon) | resource |
| [huaweicloud_cce_cluster.this](https://registry.terraform.io/providers/huaweicloud/huaweicloud/1.31.0/docs/resources/cce_cluster) | resource |
| [huaweicloud_cce_node_pool.this](https://registry.terraform.io/providers/huaweicloud/huaweicloud/1.31.0/docs/resources/cce_node_pool) | resource |
| [huaweicloud_cce_addon_template.ingress](https://registry.terraform.io/providers/huaweicloud/huaweicloud/1.31.0/docs/data-sources/cce_addon_template) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_addon_ingress_config"></a> [addon\_ingress\_config](#input\_addon\_ingress\_config) | nginx config for nginx-ingress addon | `map(any)` | `{}` | no |
| <a name="input_addon_ingress_enable"></a> [addon\_ingress\_enable](#input\_addon\_ingress\_enable) | If you need nginx-ingress addon | `bool` | `false` | no |
| <a name="input_addon_ingress_loadbalancer_ip"></a> [addon\_ingress\_loadbalancer\_ip](#input\_addon\_ingress\_loadbalancer\_ip) | Load balancer ip for nginx-ingress addon | `string` | `""` | no |
| <a name="input_addon_ingress_resource"></a> [addon\_ingress\_resource](#input\_addon\_ingress\_resource) | nginx resource for nginx-ingress addon | `map(any)` | <pre>{<br>  "limitsCpu": "1024m",<br>  "limitsMem": "1024Mi",<br>  "name": "nginx-ingress",<br>  "requestsCpu": "256m",<br>  "requestsMem": "256Mi"<br>}</pre> | no |
| <a name="input_flavor_id"></a> [flavor\_id](#input\_flavor\_id) | Flavor of the cce cluster | `string` | `"cce.s2.small"` | no |
| <a name="input_name"></a> [name](#input\_name) | Name of the cce cluster | `any` | n/a | yes |
| <a name="input_node_pool"></a> [node\_pool](#input\_node\_pool) | cce node pool feature | `map` | <pre>{<br>  "simple": {<br>    "flavor_id": "s3.large.4",<br>    "name": "generic",<br>    "os": "EulerOS 2.5"<br>  }<br>}</pre> | no |
| <a name="input_node_pool_key_pair"></a> [node\_pool\_key\_pair](#input\_node\_pool\_key\_pair) | public ssh key of cce node pool | `any` | n/a | yes |
| <a name="input_subnet_id"></a> [subnet\_id](#input\_subnet\_id) | Id of the subnet | `any` | n/a | yes |
| <a name="input_vpc_id"></a> [vpc\_id](#input\_vpc\_id) | Id of the vpc | `any` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_certificate_clusters"></a> [certificate\_clusters](#output\_certificate\_clusters) | certificate of cce cluster |
| <a name="output_certificate_users"></a> [certificate\_users](#output\_certificate\_users) | certificate users of cce cluster |
| <a name="output_kubeconfig"></a> [kubeconfig](#output\_kubeconfig) | kubeconfig file of cce cluster |
