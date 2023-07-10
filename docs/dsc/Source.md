---
parent: DSC
---

# Source

The `Source` DSC resource is used to configure AnyPackage package sources.

## Syntax

```text
Source [String] #ResourceName
{
    Location = [string]
    Name = [string]
    Provider = [string]
    [AdditionalParameters = [HashTable]]
    [Ensure = [string]{ Absent | Present }]
    [Trusted = [bool]]
}
```

## Properties

### AdditionalParameters

Specifies provider dynamic parameters.

```yaml
Attribute: Write
Type: HashTable
Default value: None
```

### Ensure

Specifies if the package source should be present.

```yaml
Attribute: Write
Type: bool
Default value: Present
```

### Location

Specifies the package source location.

```yaml
Attribute: Required
Type: string
Default value: None
```

### Name

Specifies the package source name.

```yaml
Attribute: Key
Type: string
Default value: None
```

### Provider

Specifies the package provider full name.
The provider full name is in the following format: ModuleName\ProviderName.
For AnyPackage PSResourceGet provider it would be: AnyPackage.PSResourceGet\PSResourceGet.

```yaml
Attribute: Key
Type: string
Default value: None
```

### Reasons

Returns reasons why the resource is not in compliance.
The `Code` property is the unique identifier and `Phrase` property is the human readable reason.

```yaml
Attribute: Read
Type: string
Default value: N/A
```

### Trusted

Specifies if the package source is trusted.
If set to `true` it prevents interactive untrusted source prompts.

```yaml
Attribute: Write
Type: string
Default value: False
```
