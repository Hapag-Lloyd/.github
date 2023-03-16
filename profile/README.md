# Hapag-Lloyd AG

Welcome to the Hapag-Lloyd GitHub profile page! We are a global leader in container shipping and a proud advocate of open source technology.

At Hapag-Lloyd, we recognize the value and potential of open source software. By leveraging the collective knowledge and expertise of developers worldwide, we can accelerate innovation, increase efficiency, and improve the overall quality of our services.

Our open source strategy is built on four key principles:

- Collaboration: We believe in working together with the open source community to create better solutions for our customers. We actively contribute to open source projects, share our expertise, and engage in constructive dialogue with other developers.

- Transparency: We are committed to open communication and transparency. We share our code, documentation, and development processes with the public, so that everyone can benefit from our work.

- Innovation: We are constantly seeking new and innovative ways to improve our services, and we believe that open source technology is a key driver of innovation. By embracing open source, we can tap into a vast network of developers and build upon their ideas.

- Quality: We are dedicated to delivering the highest quality services to our customers. By using open source software, we can benefit from the expertise of a diverse and talented community of developers, who can help us to identify and fix issues quickly.

At Hapag-Lloyd, we are committed to building a strong and vibrant open source community. We welcome contributions from developers of all backgrounds and skill levels, and we encourage you to explore our repositories and get involved in our projects.

Thank you for visiting our GitHub profile page, and we look forward to collaborating with you!

## Become a member (employees only)

Please create a merge request in our internal repository "Infrastructure - Hapag-Lloyd GitHub Organization". Add a new resource to the file `members.tf` as shown below.

```hcl
resource "github_membership" "first_last_name" {
  username = "github_user_id"
  role     = "member"
}
```

## Setup a new repository

Please create a merge request in our internal repository "Infrastructure - Hapag-Lloyd GitHub Organization". Add a new resource to the file `repositories` as shown below. You benefit from a standard setup providing you with common workflows, label setup and branch protections.

```hcl
# owner: <names / HL user ids> of the owners
module "descriptive_repository_name" {
  source = "./modules/default_repository"

  type = "terraform-module" # e.g. java, terraform-module

  name        = "github-repository-name"
  description = "Some sentences describing the contents."
  topics      = ["some", "github", "topics", "to", "add"]
}
```
