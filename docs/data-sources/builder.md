---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "airdrop_builder Data Source - terraform-provider-airdrop"
subcategory: ""
description: |-
  
---

# airdrop_builder (Data Source)



## Example Usage

```terraform
data "airdrop_builder" "current" {
  metadata {
    name      = "production-cluster"
    namespace = "default"
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `metadata` (Block List) (see [below for nested schema](#nestedblock--metadata))
- `timeouts` (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-Only

- `id` (String) The ID of this resource.
- `spec` (List of Object) (see [below for nested schema](#nestedatt--spec))
- `status` (List of Object) (see [below for nested schema](#nestedatt--status))

<a id="nestedblock--metadata"></a>
### Nested Schema for `metadata`

Required:

- `name` (String) Name is the name of the resource.
- `namespace` (String) Namespace is the namespace of the resource.

Optional:

- `annotations` (Map of String) Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects.
- `labels` (Map of String) Labels are key value pairs that may be used to scope and select individual resources. They are not queryable and should be preserved when modifying objects.

Read-Only:

- `creation_timestamp` (String) CreationTimestamp is a timestamp representing the server time when this object was created.
- `resource_version` (String) ResourceVersion is an opaque value that changes on every update to a resource.
- `update_timestamp` (String) UpdateTimestamp is a timestamp representing the server time when this object was last updated.


<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- `default` (String)


<a id="nestedatt--spec"></a>
### Nested Schema for `spec`

Read-Only:

- `delete_ref` (List of Object) (see [below for nested schema](#nestedobjatt--spec--delete_ref))
- `deploy_ref` (List of Object) (see [below for nested schema](#nestedobjatt--spec--deploy_ref))
- `status_ref` (List of Object) (see [below for nested schema](#nestedobjatt--spec--status_ref))
- `variables_ref` (List of Object) (see [below for nested schema](#nestedobjatt--spec--variables_ref))

<a id="nestedobjatt--spec--delete_ref"></a>
### Nested Schema for `spec.delete_ref`

Read-Only:

- `name` (String)


<a id="nestedobjatt--spec--deploy_ref"></a>
### Nested Schema for `spec.deploy_ref`

Read-Only:

- `name` (String)


<a id="nestedobjatt--spec--status_ref"></a>
### Nested Schema for `spec.status_ref`

Read-Only:

- `name` (String)


<a id="nestedobjatt--spec--variables_ref"></a>
### Nested Schema for `spec.variables_ref`

Read-Only:

- `name` (String)



<a id="nestedatt--status"></a>
### Nested Schema for `status`

Read-Only:

- `patch_session` (List of Object) (see [below for nested schema](#nestedobjatt--status--patch_session))
- `status` (String)
- `variables` (List of Object) (see [below for nested schema](#nestedobjatt--status--variables))

<a id="nestedobjatt--status--patch_session"></a>
### Nested Schema for `status.patch_session`

Read-Only:

- `patch_session_id` (String)
- `request_id` (String)
- `type` (String)


<a id="nestedobjatt--status--variables"></a>
### Nested Schema for `status.variables`

Read-Only:

- `default_variables` (String)
- `json_schema` (String)
- `venus_form` (String)
