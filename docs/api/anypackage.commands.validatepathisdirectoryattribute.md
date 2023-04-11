# ValidatePathIsDirectoryAttribute

Namespace: AnyPackage.Commands

The path is directory parameter validator.

```csharp
public sealed class ValidatePathIsDirectoryAttribute : System.Management.Automation.ValidateArgumentsAttribute
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) → CmdletMetadataAttribute → ValidateArgumentsAttribute → [ValidatePathIsDirectoryAttribute](./anypackage.commands.validatepathisdirectoryattribute.md)

## Properties

### **TypeId**

```csharp
public object TypeId { get; }
```

#### Property Value

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

## Constructors

### **ValidatePathIsDirectoryAttribute()**

```csharp
public ValidatePathIsDirectoryAttribute()
```

## Methods

### **Validate(Object, EngineIntrinsics)**

```csharp
protected void Validate(object arguments, EngineIntrinsics engineIntrinsics)
```

#### Parameters

`arguments` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

`engineIntrinsics` EngineIntrinsics<br>
