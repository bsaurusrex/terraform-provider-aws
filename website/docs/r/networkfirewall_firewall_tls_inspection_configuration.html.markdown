---
subcategory: "Network Firewall"
layout: "aws"
page_title: "AWS: aws_networkfirewall_firewall_tls_inspection_configuration"
description: |-
  Terraform resource for managing an AWS Network Firewall Firewall Tls Inspection Configuration.
---
<!---
TIP: A few guiding principles for writing documentation:
1. Use simple language while avoiding jargon and figures of speech.
2. Focus on brevity and clarity to keep a reader's attention.
3. Use active voice and present tense whenever you can.
4. Document your feature as it exists now; do not mention the future or past if you can help it.
5. Use accessible and inclusive language.
--->`
# Resource: aws_networkfirewall_firewall_tls_inspection_configuration

Terraform resource for managing an AWS Network Firewall Firewall TLS Inspection Configuration.

## Example Usage

### Basic Usage

```terraform
resource "aws_networkfirewall_firewall_tls_inspection_configuration" "example" {
  name = "example"
  description = "example"

  tls_inspection_configuration {
    server_certificate_configurations {
      certificate_authority_arn = "string
        check_certificate_revocation_status {
          revoked_status_action = "string"
          unknown_status_action = "string"
        }
      scopes {
        destination_ports {
          from_port = 0
          to_port = 65535
        }
        destinations {
          address_definition = "0.0.0.0/0"
        }
        source_ports {
          from_port = 443
          to_port = 443
        }
        sources {
          address_definition = "0.0.0.0/0"
        }
        protocols = ["number"]
      }
      server_certificates {
        resource_arn = "string"
      }
    }
  }

  encryption_configuration {
    key_id = "string"
    type   = "string"
  }

  tags = {
    Tag1 = "Value1"
    Tag2 = "Value2"
  }
}
```

## Argument Reference

The following arguments are required:

* `example_arg` - (Required) Concise argument description. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.

The following arguments are optional:

* `optional_arg` - (Optional) Concise argument description. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.
* `tags` - (Optional) A map of tags assigned to the WorkSpaces Connection Alias. If configured with a provider [`default_tags` configuration block](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#default_tags-configuration-block) present, tags with matching keys will overwrite those defined at the provider-level.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `arn` - ARN of the Firewall Tls Inspection Configuration. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.
* `example_attribute` - Concise description. Do not begin the description with "An", "The", "Defines", "Indicates", or "Specifies," as these are verbose. In other words, "Indicates the amount of storage," can be rewritten as "Amount of storage," without losing any information.
* `tags_all` - A map of tags assigned to the resource, including those inherited from the provider [`default_tags` configuration block](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#default_tags-configuration-block).

## Timeouts

[Configuration options](https://developer.hashicorp.com/terraform/language/resources/syntax#operation-timeouts):

* `create` - (Default `60m`)
* `update` - (Default `180m`)
* `delete` - (Default `90m`)

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import Network Firewall Firewall Tls Inspection Configuration using the `example_id_arg`. For example:

```terraform
import {
  to = aws_networkfirewall_firewall_tls_inspection_configuration.example
  id = "firewall_tls_inspection_configuration-id-12345678"
}
```

Using `terraform import`, import Network Firewall Firewall Tls Inspection Configuration using the `example_id_arg`. For example:

```console
% terraform import aws_networkfirewall_firewall_tls_inspection_configuration.example firewall_tls_inspection_configuration-id-12345678
```
