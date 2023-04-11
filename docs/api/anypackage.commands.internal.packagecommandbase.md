---
parent: API
---

# PackageCommandBase

Namespace: AnyPackage.Commands.Internal

The base class for package commands.

```csharp
public abstract class PackageCommandBase : CommandBase, System.Management.Automation.IDynamicParameters
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → InternalCommand → Cmdlet → PSCmdlet → [CommandBase](./anypackage.commands.internal.commandbase.md) → [PackageCommandBase](./anypackage.commands.internal.packagecommandbase.md)<br>
Implements IDynamicParameters

## Properties

### **Provider**

Gets or sets the package provider.

```csharp
public abstract string Provider { get; set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Events**

```csharp
public PSEventManager Events { get; }
```

#### Property Value

PSEventManager<br>

### **Host**

```csharp
public PSHost Host { get; }
```

#### Property Value

PSHost<br>

### **InvokeCommand**

```csharp
public CommandInvocationIntrinsics InvokeCommand { get; }
```

#### Property Value

CommandInvocationIntrinsics<br>

### **InvokeProvider**

```csharp
public ProviderIntrinsics InvokeProvider { get; }
```

#### Property Value

ProviderIntrinsics<br>

### **JobManager**

```csharp
public JobManager JobManager { get; }
```

#### Property Value

JobManager<br>

### **JobRepository**

```csharp
public JobRepository JobRepository { get; }
```

#### Property Value

JobRepository<br>

### **MyInvocation**

```csharp
public InvocationInfo MyInvocation { get; }
```

#### Property Value

InvocationInfo<br>

### **PagingParameters**

```csharp
public PagingParameters PagingParameters { get; }
```

#### Property Value

PagingParameters<br>

### **ParameterSetName**

```csharp
public string ParameterSetName { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **SessionState**

```csharp
public SessionState SessionState { get; }
```

#### Property Value

SessionState<br>

### **CommandRuntime**

```csharp
public ICommandRuntime CommandRuntime { get; set; }
```

#### Property Value

ICommandRuntime<br>

### **Stopping**

```csharp
public bool Stopping { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **CommandOrigin**

```csharp
public CommandOrigin CommandOrigin { get; }
```

#### Property Value

CommandOrigin<br>

## Methods

### **SetRequest()**

Sets the request property.

```csharp
protected void SetRequest()
```

### **SetRequest(String, PackageVersionRange, String, Boolean)**

Sets the request property.

```csharp
protected void SetRequest(string name, PackageVersionRange version, string source, bool trustSource)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the package name.

`version` [PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>
Specifies the package version.

`source` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the package source.

`trustSource` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Specifies if the source should be trusted.

### **SetRequest(PackageInfo, Boolean)**

Sets the request property.

```csharp
protected void SetRequest(PackageInfo package, bool trustSource)
```

#### Parameters

`package` [PackageInfo](./anypackage.provider.packageinfo.md)<br>
Specifies the package.

`trustSource` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
Specifies if the source should be trusted.

### **SetRequest(Uri)**

Sets the request property.

```csharp
protected void SetRequest(Uri uri)
```

#### Parameters

`uri` Uri<br>
Specifies the package uri.

### **SetPathRequest(String)**

Sets the request property.

```csharp
protected void SetPathRequest(string path)
```

#### Parameters

`path` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the path.

### **GetNameInstances(String)**

Gets provider instances.

```csharp
protected IEnumerable<PackageProvider> GetNameInstances(string name)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Name of the provider.

#### Returns

[IEnumerable&lt;PackageProvider&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetPathInstances(String)**

Gets provider instances for a given path.

```csharp
protected IEnumerable<PackageProvider> GetPathInstances(string path)
```

#### Parameters

`path` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The path.

#### Returns

[IEnumerable&lt;PackageProvider&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetUriInstances(Uri)**

Get provider instances for a given Uri.

```csharp
protected IEnumerable<PackageProvider> GetUriInstances(Uri uri)
```

#### Parameters

`uri` Uri<br>
The Uri.

#### Returns

[IEnumerable&lt;PackageProvider&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **GetPaths(IEnumerable&lt;String&gt;, Boolean)**

Gets normalized paths.

```csharp
protected IEnumerable<string> GetPaths(IEnumerable<string> paths, bool expandWildcards)
```

#### Parameters

`paths` [IEnumerable&lt;String&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>
The paths to normalize.

`expandWildcards` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If wildcards should be expanded.

#### Returns

[IEnumerable&lt;String&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **FilterSource(String, IEnumerable&lt;PackageProvider&gt;)**

Filters package providers by the source.

```csharp
protected IEnumerable<PackageProvider> FilterSource(string source, IEnumerable<PackageProvider> providers)
```

#### Parameters

`source` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The source.

`providers` [IEnumerable&lt;PackageProvider&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>
The providers.

#### Returns

[IEnumerable&lt;PackageProvider&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

### **ValidateFile(String, ProviderInfo)**

Validates that the path is a file.

```csharp
protected bool ValidateFile(string path, ProviderInfo provider)
```

#### Parameters

`path` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The path.

`provider` ProviderInfo<br>
The PS provider.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **ValidateOperation(PackageInfo, PackageProviderOperations)**

Validates that the package provider supports the operation.

```csharp
protected bool ValidateOperation(PackageInfo package, PackageProviderOperations operation)
```

#### Parameters

`package` [PackageInfo](./anypackage.provider.packageinfo.md)<br>
Package to validate.

`operation` [PackageProviderOperations](./anypackage.provider.packageprovideroperations.md)<br>
Operation to validate.

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **Invoke(String, String, IDictionary&lt;PackageProvider, InvokePackage&gt;, Boolean, Boolean)**

Invokes the package operation on multiple package instances.

```csharp
protected void Invoke(string package, string verb, IDictionary<PackageProvider, InvokePackage> instances, bool shouldProcess, bool first)
```

#### Parameters

`package` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The package label.

`verb` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
The package operation.

`instances` [IDictionary&lt;PackageProvider, InvokePackage&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2)<br>
The package instance and operation.

`shouldProcess` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If should call ShouldProcess.

`first` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If should only process first provider.
