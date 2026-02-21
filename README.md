# aap-organizations-global

Organization definitions and repos-manifest.yml registry

## CasC Key

```
aap_organizations
```

## Usage

Place JSON files in this repository using the `aap_organizations` key.
The CasC dispatcher will automatically pick up and apply these configurations
to AAP when the CI/CD pipeline triggers.

### Example

```json
{
    "aap_organizations": [
        {
            "name": "example-resource",
            "description": "Replace with your actual configuration"
        }
    ]
}
```

## CI/CD Pipeline

This repository includes a thin CI/CD caller that triggers the platform's
shared CasC pipeline on push and pull request events. The pipeline validates
JSON files and triggers the dispatcher Job Template in AAP.

## Registry

This repository also contains `repos-manifest.yml`, the central registry of
all CasC repositories (platform and tenant). The dispatcher reads this manifest
to determine which repos to clone and process.

## Part of the Hybrid CasC Solution

This repository is managed by the **aap-casc-platform-demo** platform team as part
of the Hybrid AAP Configuration-as-Code framework. See the
[aap-casc-engine](../aap-casc-engine) repository
for full documentation.
