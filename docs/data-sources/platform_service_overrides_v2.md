---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_platform_service_overrides_v2 Data Source - terraform-provider-harness"
subcategory: "Next Gen"
description: |-
  Data source for Harness service overrides V2.
---

# harness_platform_service_overrides_v2 (Data Source)

Data source for Harness service overrides V2.

## Example Usage

```terraform
data "harness_platform_service_overrides_v2" "test" {
  identifier = "identifier"
  org_id     = "orgIdentifier"
  project_id = "projectIdentifier"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `identifier` (String) The identifier of the override entity.

### Optional

- `org_id` (String) Unique identifier of the organization.
- `project_id` (String) Unique identifier of the project.

### Read-Only

- `id` (String) The ID of this resource.
- `infra_id` (String) The infrastructure ID to which the override entity is associated.
- `service_id` (String) The service ID to which the override entity is associated.
- `env_id` (String) The environment ID to which the override entity is associated.
- `type` (String) The type of the override entity.
- `yaml` (String) The yaml of the override entity's spec property. More details regarding the spec property can be found [here](https://apidocs.harness.io/tag/ServiceOverrides#operation/createServiceOverride!path=spec&t=request)
