---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "harness_autostopping_schedule Data Source - terraform-provider-harness"
subcategory: "Next Gen"
description: |-
  Data source for retrieving a fixed schedule for Harness AutoStopping rule
---

# harness_autostopping_schedule (Data Source)

Data source for retrieving a fixed schedule for Harness AutoStopping rule



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `schedule_type` (String) Type of the schedule. Valid values are `uptime` and `downtime`

### Read-Only

- `ending_on` (String) Time until which schedule will be active. Need to be in YYYY-MM-DD HH:mm:SS format. Eg 2006-01-02 15:04:05
- `id` (String) The ID of this resource.
- `identifier` (Number) Unique identifier of the schedule
- `name` (String) Name of the schedule
- `repeats` (List of Object) For defining periodic schedule. Periodic nature will be applicable from the time of creation of schedule, unless specific 'time_period' is specified (see [below for nested schema](#nestedatt--repeats))
- `rules` (List of Number) ID of AutoStopping rules on which the schedule applies
- `starting_from` (String) Time from which schedule will be active. Schedule will take immediate effect if starting_from is not specified. Need to be in YYYY-MM-DD HH:mm:SS format. Eg 2006-01-02 15:04:05
- `time_zone` (String) Time zone in which schedule needs to be executed

<a id="nestedatt--repeats"></a>
### Nested Schema for `repeats`

Read-Only:

- `days` (String)
- `end_time` (String)
- `start_time` (String)
