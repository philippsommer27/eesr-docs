# Reporting Profiles

The EESR metrics and graphs library features over 8 different options to choose from. Although all of these can be reported through the dashboard view, in the standard and compact view there is only enough space to present a selection of the available information. Reporting profiles allow us to define which key information should be presented on the report.&#x20;

### What is in a reporting profile?

Reporting profiles are represented as JSON files defined by the following JSON Schema:

```json
{
    "$schema": "https://json-schema.org/draft/2020-12/schema",
    "$id" : "https://github.com/philippsommer27/opendc-eesr/blob/main/eesr/reporting/library/schemas/profile_schema.json",
    "title": "OpenDC EESR Profile Schema",
    "description": "JSON schema definition for defining a reporting profile",
    "type" : "object",
    "properties": {
        "name" : {
            "description" : "The name of the custom reporting profile",
            "type" : "string"
        },
        "builtin_metrics" : {
            "description" : "List of metric IDs from the EESR metrics library to report",
            "type" : "array",
            "items" : {
                "type" : "string",
                "uniqueItems": true,
                "enum" : [
                    "PUE",
                    "CUE",
                    "APCr",
                    "CO2 (kg)",
                    "GEC (green)",
                    "GEC (ren)",
                    "TUE",
                    "NeNr",
                    "total_energy",
                    "CADE",
                    "DPPE"
                ]
            }
        },
        "additional_metrics" : {
            "description" : "List of metric IDs that should included in additional_metrics in input file",
            "type" : "array",
            "uniqueItems": true,
            "items" : {
                "type" : "string"
            }
        },
        "graph" : {
            "description" : "Graph to generate and display in the report (unless custom graph)",
            "type" : "string"
        }
    },
    "required": ["name", "builtin_metrics", "graph"]
}
```



### Packaged Profiles

Currently EESR defines 3 reporting profiles.

{% content-ref url="standard-0.1.md" %}
[standard-0.1.md](standard-0.1.md)
{% endcontent-ref %}

{% content-ref url="efficiency-0.1.md" %}
[efficiency-0.1.md](efficiency-0.1.md)
{% endcontent-ref %}

{% content-ref url="sustainability-0.1.md" %}
[sustainability-0.1.md](sustainability-0.1.md)
{% endcontent-ref %}
