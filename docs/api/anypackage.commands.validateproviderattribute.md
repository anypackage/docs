# ValidateProviderAttribute

Namespace: AnyPackage.Commands

The provider parameter validator.

```csharp
public sealed class ValidateProviderAttribute : System.Management.Automation.ValidateArgumentsAttribute
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) → CmdletMetadataAttribute → ValidateArgumentsAttribute → [ValidateProviderAttribute](./anypackage.commands.validateproviderattribute.md)

## Properties

### **TypeId**

```csharp
public object TypeId { get; }
```

#### Property Value

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

## Constructors

### **ValidateProviderAttribute(PackageProviderOperations)**

Instantiates the `ValidateProviderAttribute` class.

```csharp
public ValidateProviderAttribute(PackageProviderOperations operations)
```

#### Parameters

`operations` [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>
Specifies the package provider operation.

## Methods

### **Validate(Object, EngineIntrinsics)**

```csharp
protected void Validate(object arguments, EngineIntrinsics engineIntrinsics)
```

#### Parameters

`arguments` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

`engineIntrinsics` EngineIntrinsics<br>
