---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "datadog_security_monitoring_rules Data Source - terraform-provider-datadog"
subcategory: ""
description: |-
  Use this data source to retrieve information about existing security monitoring rules for use in other resources.
---

# datadog_security_monitoring_rules (Data Source)

Use this data source to retrieve information about existing security monitoring rules for use in other resources.

## Example Usage

```terraform
data "datadog_security_monitoring_rules" "test" {
  name_filter         = "attack"
  tags_filter         = ["foo:bar"]
  default_only_filter = true
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- **default_only_filter** (Boolean) Limit the search to default rules
- **name_filter** (String) A rule name to limit the search
- **tags_filter** (List of String) A list of tags to limit the search
- **user_only_filter** (Boolean) Limit the search to user rules

### Read-only

- **id** (String) The ID of this resource.
- **rule_ids** (List of String) List of IDs of the matched rules.
- **rules** (List of Object) List of rules. (see [below for nested schema](#nestedatt--rules))

<a id="nestedatt--rules"></a>
### Nested schema for `rules`

Read-only:

- **case** (List of Object) (see [below for nested schema](#nestedobjatt--rules--case))
- **enabled** (Boolean)
- **filter** (List of Object) (see [below for nested schema](#nestedobjatt--rules--filter))
- **has_extended_title** (Boolean)
- **message** (String)
- **name** (String)
- **options** (List of Object) (see [below for nested schema](#nestedobjatt--rules--options))
- **query** (List of Object) (see [below for nested schema](#nestedobjatt--rules--query))
- **tags** (List of String)
- **type** (String)

<a id="nestedobjatt--rules--case"></a>
### Nested schema for `rules.case`

Read-only:

- **condition** (String)
- **name** (String)
- **notifications** (List of String)
- **status** (String)


<a id="nestedobjatt--rules--filter"></a>
### Nested schema for `rules.filter`

Read-only:

- **action** (String)
- **query** (String)


<a id="nestedobjatt--rules--options"></a>
### Nested schema for `rules.options`

Read-only:

- **detection_method** (String)
- **evaluation_window** (Number)
- **keep_alive** (Number)
- **max_signal_duration** (Number)
- **new_value_options** (List of Object) (see [below for nested schema](#nestedobjatt--rules--options--new_value_options))

<a id="nestedobjatt--rules--options--new_value_options"></a>
### Nested schema for `rules.options.new_value_options`

Read-only:

- **forget_after** (Number)
- **learning_duration** (Number)



<a id="nestedobjatt--rules--query"></a>
### Nested schema for `rules.query`

Read-only:

- **agent_rule** (List of Object) (see [below for nested schema](#nestedobjatt--rules--query--agent_rule))
- **aggregation** (String)
- **distinct_fields** (List of String)
- **group_by_fields** (List of String)
- **metric** (String)
- **name** (String)
- **query** (String)

<a id="nestedobjatt--rules--query--agent_rule"></a>
### Nested schema for `rules.query.agent_rule`

Read-only:

- **agent_rule_id** (String)
- **expression** (String)


