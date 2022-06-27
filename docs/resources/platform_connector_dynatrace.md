---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_platform_connector_dynatrace Resource - terraform-provider-harness"
subcategory: ""
description: |-
  Resource for creating a Dynatrace connector.
---

# harness_platform_connector_dynatrace (Resource)

Resource for creating a Dynatrace connector.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `api_token_ref` (String) The reference to the Harness secret containing the api token.
- `identifier` (String) Unique identifier of the resource.
- `name` (String) Name of the resource.
- `url` (String) Url of the Dynatrace server.

### Optional

- `delegate_selectors` (Set of String) Connect using only the delegates which have these tags.
- `description` (String) Description of the resource.
- `id` (String) The ID of this resource.
- `org_id` (String) Unique identifier of the organization.
- `project_id` (String) Unique identifier of the project.
- `tags` (Set of String) Tags to associate with the resource. Tags should be in the form `name:value`.

