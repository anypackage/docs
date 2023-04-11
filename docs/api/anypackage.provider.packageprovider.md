---
parent: API
---

# PackageProvider

Namespace: AnyPackage.Provider

The `PackageProvider` class.

```csharp
public abstract class PackageProvider
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageProvider](./anypackage.provider.packageprovider.md)

## Properties

### **ProviderInfo**

Gets the package provider information.

```csharp
public PackageProviderInfo ProviderInfo { get; internal set; }
```

#### Property Value

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

**Remarks:**

If a derived type of `PackageProviderInfo` was returned from the `Initialize` method, it
 will be set here in all subsequent calls to the provider.

## Methods

### **Initialize(PackageProviderInfo)**

Performs one time initialization for the package provider during registration.

```csharp
protected PackageProviderInfo Initialize(PackageProviderInfo providerInfo)
```

#### Parameters

`providerInfo` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

#### Returns

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

            Returns PackageProviderInfo or derived type that can be used
            to present new properties or methods to the user.
            It can also be used maintain state or cache between instances of
            the package provider.

### **Initialize()**

```csharp
internal void Initialize()
```

### **Clean()**

Performs one time clean up of the package provider during unregistration.

```csharp
protected internal void Clean()
```

### **GetDynamicParameters(String)**

Gets the dynamic parameters for command name.

```csharp
protected internal object GetDynamicParameters(string commandName)
```

#### Parameters

`commandName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The cmdlet name.

#### Returns

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

            The method can be overwritten to return an object
            or a RuntimeDefinedParameterDictionary.

### **IsSource(String)**

Gets if the source is supported by the provider.

```csharp
protected internal bool IsSource(string source)
```

#### Parameters

`source` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The source parameter from cmdlets.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Returns true if source is supported.

**Remarks:**

The default implementation returns `true`.

### **IsSupportedFileExtension(String)**

```csharp
internal bool IsSupportedFileExtension(string extension)
```

#### Parameters

`extension` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **IsSupportedUriScheme(String)**

```csharp
internal bool IsSupportedUriScheme(string extension)
```

#### Parameters

`extension` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **FindPackage(PackageRequest)**

```csharp
internal void FindPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **GetPackage(PackageRequest)**

```csharp
internal void GetPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **InstallPackage(PackageRequest)**

```csharp
internal void InstallPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **SavePackage(PackageRequest)**

```csharp
internal void SavePackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **PublishPackage(PackageRequest)**

```csharp
internal void PublishPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **UninstallPackage(PackageRequest)**

```csharp
internal void UninstallPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **UpdatePackage(PackageRequest)**

```csharp
internal void UpdatePackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>

### **GetSource(SourceRequest)**

```csharp
internal void GetSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>

### **RegisterSource(SourceRequest)**

```csharp
internal void RegisterSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>

### **SetSource(SourceRequest)**

```csharp
internal void SetSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>

### **UnregisterSource(SourceRequest)**

```csharp
internal void UnregisterSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>
