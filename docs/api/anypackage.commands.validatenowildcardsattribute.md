---
parent: API
---

# ValidateNoWildcardsAttribute

Namespace: AnyPackage.Commands

The no wildcards parameter validator.

```csharp
public sealed class ValidateNoWildcardsAttribute : System.Management.Automation.ValidateArgumentsAttribute
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) → CmdletMetadataAttribute → ValidateArgumentsAttribute → [ValidateNoWildcardsAttribute](./anypackage.commands.validatenowildcardsattribute.md)

## Properties

### **TypeId**

```csharp
public object TypeId { get; }
```

#### Property Value

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

## Constructors

### **ValidateNoWildcardsAttribute()**

```csharp
public ValidateNoWildcardsAttribute()
```

## Methods

### **Validate(Object, EngineIntrinsics)**

```csharp
protected void Validate(object arguments, EngineIntrinsics engineIntrinsics)
```

#### Parameters

`arguments` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

`engineIntrinsics` EngineIntrinsics<br>
