# Flat No More! Hierarchical Multitenancy and Projects Acting as Domains in OpenStack

## User management

Can use role assignment to control deletion

## Domain

Uses top level domain to control access and usage of clouds

Controlled by

```
"is_domiain": false
"parent_id": lsd_id # (our atmo id)
```

LSD -> Openstack -> Keystone
OS has parent of LSD and keystone has OS as parent

## Nested Quota

Works with Cinder
Under review in Nova


