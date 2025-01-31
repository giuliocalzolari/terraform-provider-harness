---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_platform_connector_aws Data Source - terraform-provider-harness"
subcategory: "Next Gen"
description: |-
  Datasource for looking up an AWS connector.
---

# harness_platform_connector_aws (Data Source)

Datasource for looking up an AWS connector.

## Example Usage

```terraform
data "harness_platform_connector_aws" "example" {
  identifier = "identifier"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `identifier` (String) Unique identifier of the resource.

### Optional

- `name` (String) Name of the resource.
- `org_id` (String) Unique identifier of the organization.
- `project_id` (String) Unique identifier of the project.

### Read-Only

- `cross_account_access` (List of Object) Select this option if you want to use one AWS account for the connection, but you want to deploy or build in a different AWS account. In this scenario, the AWS account used for AWS access in Credentials will assume the IAM role you specify in Cross-account role ARN setting. This option uses the AWS Security Token Service (STS) feature. (see [below for nested schema](#nestedatt--cross_account_access))
- `description` (String) Description of the resource.
- `equal_jitter_backoff_strategy` (List of Object) Equal Jitter BackOff Strategy. (see [below for nested schema](#nestedatt--equal_jitter_backoff_strategy))
- `fixed_delay_backoff_strategy` (List of Object) Fixed Delay BackOff Strategy. (see [below for nested schema](#nestedatt--fixed_delay_backoff_strategy))
- `full_jitter_backoff_strategy` (List of Object) Full Jitter BackOff Strategy. (see [below for nested schema](#nestedatt--full_jitter_backoff_strategy))
- `id` (String) The ID of this resource.
- `inherit_from_delegate` (List of Object) Inherit credentials from the delegate. (see [below for nested schema](#nestedatt--inherit_from_delegate))
- `irsa` (List of Object) Use IAM role for service accounts. (see [below for nested schema](#nestedatt--irsa))
- `manual` (List of Object) Use IAM role for service accounts. (see [below for nested schema](#nestedatt--manual))
- `tags` (Set of String) Tags to associate with the resource.

<a id="nestedatt--cross_account_access"></a>
### Nested Schema for `cross_account_access`

Read-Only:

- `external_id` (String) If the administrator of the account to which the role belongs provided you with an external ID, then enter that value.
- `role_arn` (String) The Amazon Resource Name (ARN) of the role that you want to assume. This is an IAM role in the target AWS account.


<a id="nestedatt--equal_jitter_backoff_strategy"></a>
### Nested Schema for `equal_jitter_backoff_strategy`

Read-Only:

- `base_delay` (Number) Base delay.
- `max_backoff_time` (Number) Max BackOff Time.
- `retry_count` (Number) Retry Count.


<a id="nestedatt--fixed_delay_backoff_strategy"></a>
### Nested Schema for `fixed_delay_backoff_strategy`

Read-Only:

- `fixed_backoff` (Number) Fixed Backoff.
- `retry_count` (Number) Retry Count.


<a id="nestedatt--full_jitter_backoff_strategy"></a>
### Nested Schema for `full_jitter_backoff_strategy`

Read-Only:

- `base_delay` (Number) Base delay.
- `max_backoff_time` (Number) Max BackOff Time.
- `retry_count` (Number) Retry Count.


<a id="nestedatt--inherit_from_delegate"></a>
### Nested Schema for `inherit_from_delegate`

Read-Only:

- `delegate_selectors` (Set of String) The delegates to inherit the credentials from.


<a id="nestedatt--irsa"></a>
### Nested Schema for `irsa`

Read-Only:

- `delegate_selectors` (Set of String) The delegates to inherit the credentials from.


<a id="nestedatt--manual"></a>
### Nested Schema for `manual`

Read-Only:

- `access_key` (String) AWS access key.
- `access_key_ref` (String) Reference to the Harness secret containing the aws access key. To reference a secret at the organization scope, prefix 'org' to the expression: org.{identifier}. To reference a secret at the account scope, prefix 'account` to the expression: account.{identifier}.
- `delegate_selectors` (Set of String) Connect only use delegates with these tags.
- `secret_key_ref` (String) Reference to the Harness secret containing the aws secret key. To reference a secret at the organization scope, prefix 'org' to the expression: org.{identifier}. To reference a secret at the account scope, prefix 'account` to the expression: account.{identifier}.


