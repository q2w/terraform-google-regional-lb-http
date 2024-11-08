# Regional HTTP Load Balancer Terraform Module

Modular Regional HTTP Load Balancer for GCE using forwarding rules.

-   If you would like to allow for backend groups to be managed outside
    Terraform, such as via GKE services, see the [backends](./modules/backends)
    submodule.
-   If you would like to use regional load balancing with serverless backends
    (Cloud Run, Cloud Functions or App Engine), see the
    [frontend](./modules/frontend) submodule.

## Load Balancer Types

-   [TCP load balancer](https://github.com/terraform-google-modules/terraform-google-lb)
-   [HTTP/S global load balancer](https://github.com/terraform-google-modules/terraform-google-lb-http)
-   **HTTP/S reginal load balancer**
-   [Internal load balancer](https://github.com/terraform-google-modules/terraform-google-lb-internal)

## Compatibility

This module is meant for use with Terraform 1.3+ and tested using Terraform 1.3.
If you find incompatibilities using Terraform >=1.3, please open an issue. If
you haven't [upgraded](https://www.terraform.io/upgrade-guides/0-13.html) and
need a Terraform 0.12.x-compatible version of this module, the last released
version intended for Terraform 0.12.x is
[v4.5.0](https://registry.terraform.io/modules/GoogleCloudPlatform/lb-http/google/4.5.0).

## Contributing

Refer to the [contribution guidelines](./CONTRIBUTING.md) for information on
contributing to this module.
