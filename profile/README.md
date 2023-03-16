# Hapag-Lloyd AG

This is the public view of our organization.

## Become a member

Please create a merge request in our internal repository "Infrastructure - Hapag-Lloyd GitHub Organization". Add a new resource to the file `members.tf` as shown below.

```hcl
resource "github_membership" "first_last_name" {
  username = "github_user_id"
  role     = "member"
}
```
