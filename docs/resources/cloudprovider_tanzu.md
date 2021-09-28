---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_cloudprovider_tanzu Resource - terraform-provider-harness"
subcategory: ""
description: |-
  Resource for creating a Tanzu cloud provider
---

# harness_cloudprovider_tanzu (Resource)

Resource for creating a Tanzu cloud provider

## Example Usage

```terraform
data "harness_secret_manager" "default" {
  default = true
}

resource "harness_encrypted_text" "tanzu_password" {
  name              = "tanzu_password"
  value             = "<PASSWORD>"
  secret_manager_id = data.harness_secret_manager.default.id
}

resource "harness_cloudprovider_tanzu" "example" {
  name                 = "example"
  endpoint             = "https://endpoint.com"
  skip_validation      = true
  username             = "<USERNAME>"
  password_secret_name = harness_encrypted_text.tanzu_password.name
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **endpoint** (String) The url of the Tanzu platform.
- **name** (String) The name of the cloud provider.
- **password_secret_name** (String) The name of the Harness secret containing the password to use to authenticate to Tanzu.

### Optional

- **skip_validation** (Boolean) Skip validation of Tanzu configuration.
- **username** (String) The username to use to authenticate to Tanzu.
- **username_secret_name** (String) The name of the Harness secret containing the username to authenticate to Tanzu with.

### Read-Only

- **id** (String) The id of the cloud provider.

## Import

Import is supported using the following syntax:

```shell
# Import using the Harness Tanzu cloud provider id.
terraform import harness_cloudprovider_tanzu.example <provider_id>
```