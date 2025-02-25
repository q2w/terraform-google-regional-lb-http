# HTTP Internal Regional Load Balancer Example

This example creates a simple application with below components.

* *External Load Balancer*: An external regional load balancer to create an external forwarding rule. The external_ip of the forwarding rule will be used to access the application. The external load balancer routes traffic to the frontend service.
* *Frontend Service*: A cloud-run service to send request to internal regional load balancer. The cloud-run service uses VPC access connector to send the request to the internal load balancer.
* *Internal Load Balancer*: An internal regional load balancer to send traffic to internal cloud run service.
* *Backend Service*: A cloud-run service to run the actual application code. The cloud-run service can be accessed within internal traffic. The internal Application Load Balancer is considered internal traffic.


The `google_compute_region_backend_service` and its dependencies are created as part of `backend` module.
The forwarding rules and its dependecies are created as part of `frontend` modules.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| project\_id | n/a | `string` | n/a | yes |
| region | n/a | `string` | `"us-central1"` | no |

## Outputs

| Name | Description |
|------|-------------|
| external\_ip | The IP address of the forwarding rule |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
