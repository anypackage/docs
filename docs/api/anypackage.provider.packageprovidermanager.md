---
parent: API
---

# PackageProviderManager

Namespace: AnyPackage.Provider

This class is used to manage package providers.

```csharp
public static class PackageProviderManager
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageProviderManager](./anypackage.provider.packageprovidermanager.md)

## Methods

### **RegisterProvider(Guid, Type, PSModuleInfo)**

Register a package provider.

```csharp
public static void RegisterProvider(Guid id, Type type, PSModuleInfo module)
```

#### Parameters

`id` [Guid](https://docs.microsoft.com/en-us/dotnet/api/system.guid)<br>
The package provider ID.

`type` [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)<br>
The type implementing the package provider.

`module` PSModuleInfo<br>
The module associated with the package provider.

### **RegisterProvider(Guid, Type, String)**

Register a package provider.

```csharp
public static void RegisterProvider(Guid id, Type type, string moduleName)
```

#### Parameters

`id` [Guid](https://docs.microsoft.com/en-us/dotnet/api/system.guid)<br>
The package provider ID.

`type` [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)<br>
The type implementing the package provider.

`moduleName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The module name associated with the package provider.

### **UnregisterProvider(Guid)**

Unregister a package provider.

```csharp
public static void UnregisterProvider(Guid id)
```

#### Parameters

`id` [Guid](https://docs.microsoft.com/en-us/dotnet/api/system.guid)<br>
The package provider identifier.

### **GetProvider(String, PackageProviderOperations)**

```csharp
internal static PackageProviderInfo GetProvider(string name, PackageProviderOperations operations)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`operations` [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>

#### Returns

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

### **GetProviders()**

```csharp
internal static IEnumerable<PackageProviderInfo> GetProviders()
```

#### Returns

[IEnumerable&lt;PackageProviderInfo&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetProviders(String)**

```csharp
internal static IEnumerable<PackageProviderInfo> GetProviders(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[IEnumerable&lt;PackageProviderInfo&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetProviders(PackageProviderOperations)**

```csharp
internal static IEnumerable<PackageProviderInfo> GetProviders(PackageProviderOperations operations)
```

#### Parameters

`operations` [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>

#### Returns

[IEnumerable&lt;PackageProviderInfo&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetProviders(String, PackageProviderOperations)**

```csharp
internal static IEnumerable<PackageProviderInfo> GetProviders(string name, PackageProviderOperations operations)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`operations` [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>

#### Returns

[IEnumerable&lt;PackageProviderInfo&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetModuleInfo(String)**

```csharp
internal static PSModuleInfo GetModuleInfo(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

PSModuleInfo<br>
