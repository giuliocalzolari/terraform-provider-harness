---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_platform_connector_jira Resource - terraform-provider-harness"
subcategory: ""
description: |-
  Resource for creating a Jira connector.
---

# harness_platform_connector_jira (Resource)

Resource for creating a Jira connector.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `identifier` (String) Unique identifier of the resource.
- `name` (String) Name of the resource.
- `password_ref` (String) Reference to a secret containing the password to use for authentication.
- `url` (String) Url of the Jira server.

### Optional

- `delegate_selectors` (Set of String) Connect using only the delegates which have these tags.
- `description` (String) Description of the resource.
- `id` (String) The ID of this resource.
- `org_id` (String) Unique identifier of the organization.
- `project_id` (String) Unique identifier of the project.
- `tags` (Set of String) Tags to associate with the resource. Tags should be in the form `name:value`.
- `username` (String) Username to use for authentication.
- `username_ref` (String) Reference to a secret containing the username to use for authentication.

