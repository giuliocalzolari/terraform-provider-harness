---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_platform_connector_artifactory Data Source - terraform-provider-harness"
subcategory: ""
description: |-
  Resource for looking up an App Dynamics connector.
---

# harness_platform_connector_artifactory (Data Source)

Resource for looking up an App Dynamics connector.



<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `id` (String) The ID of this resource.
- `identifier` (String) Unique identifier of the resource.
- `name` (String) Name of the resource.
- `org_id` (String) Unique identifier of the organization.
- `project_id` (String) Unique identifier of the project.

### Read-Only

- `credentials` (List of Object) Credentials to use for authentication. (see [below for nested schema](#nestedatt--credentials))
- `delegate_selectors` (Set of String) Connect using only the delegates which have these tags.
- `description` (String) Description of the resource.
- `tags` (Set of String) Tags to associate with the resource. Tags should be in the form `name:value`.
- `url` (String) URL of the Artifactory server.

<a id="nestedatt--credentials"></a>
### Nested Schema for `credentials`

Read-Only:

- `password_ref` (String)
- `username` (String)
- `username_ref` (String)

