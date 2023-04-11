# PackageSourceInfo

Namespace: AnyPackage.Provider

The `PackageSourceInfo` class.
 Contains information regarding a package source.

```csharp
public sealed class PackageSourceInfo
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PackageSourceInfo](./anypackage.provider.packagesourceinfo.md)

## Properties

### **Name**

Gets the source name.

```csharp
public string Name { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Location**

Gets the source location.

```csharp
public string Location { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Provider**

Gets the package provider information.

```csharp
public PackageProviderInfo Provider { get; }
```

#### Property Value

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

### **Metadata**

Gets source metadata.

```csharp
public IReadOnlyDictionary<string, object> Metadata { get; }
```

#### Property Value

[IReadOnlyDictionary&lt;String, Object&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ireadonlydictionary-2)<br>

### **Trusted**

Gets if the source is trusted.

```csharp
public bool Trusted { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

## Constructors

### **PackageSourceInfo(String, String, PackageProviderInfo)**

Instantiates a `PackageSourceInfo` class.

```csharp
public PackageSourceInfo(string name, string location, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source name.

`location` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source location.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
If name, location, or provider is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
If name or location is empty or whitespace.

### **PackageSourceInfo(String, String, Boolean, PackageProviderInfo)**

Instantiates a `PackageSourceInfo` class.

```csharp
public PackageSourceInfo(string name, string location, bool trusted, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source name.

`location` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source location.

`trusted` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If source is trusted.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
If name, location, or provider is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
If name or location is empty or whitespace.

### **PackageSourceInfo(String, String, Boolean, IDictionary&lt;String, Object&gt;, PackageProviderInfo)**

Instantiates a `PackageSourceInfo` class.

```csharp
public PackageSourceInfo(string name, string location, bool trusted, IDictionary<string, object> metadata, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source name.

`location` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source location.

`trusted` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If source is trusted.

`metadata` [IDictionary&lt;String, Object&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2)<br>
Additional metadata about source.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
If name, location, provider, or metadata is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
If name or location is empty or whitespace.

### **PackageSourceInfo(String, String, Boolean, Hashtable, PackageProviderInfo)**

Instantiates a `PackageSourceInfo` class.

```csharp
public PackageSourceInfo(string name, string location, bool trusted, Hashtable metadata, PackageProviderInfo provider)
```

#### Parameters

`name` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source name.

`location` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Source location.

`trusted` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>
If source is trusted.

`metadata` [Hashtable](https://docs.microsoft.com/en-us/dotnet/api/system.collections.hashtable)<br>
Additional metadata about source.

`provider` [PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>
Package provider.

#### Exceptions

[ArgumentNullException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentnullexception)<br>
If name, location, provider, or metadata is null.

[ArgumentException](https://docs.microsoft.com/en-us/dotnet/api/system.argumentexception)<br>
If name or location is empty or whitespace.

**Remarks:**

Metadata hashtable keys will be converted to strings.

## Methods

### **ToString()**

Returns a string of the source name.

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

            The source name.
