---
parent: API
---

# PackageProviderNotFoundException

Namespace: AnyPackage.Provider

The `PackageProviderNotFoundException` class.

```csharp
public class PackageProviderNotFoundException : PackageProviderException, System.Runtime.Serialization.ISerializable
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) → [PackageProviderException](./anypackage.provider.packageproviderexception.md) → [PackageProviderNotFoundException](./anypackage.provider.packageprovidernotfoundexception.md)<br>
Implements [ISerializable](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.serialization.iserializable)

## Properties

### **ProviderName**

Gets the provider name.

```csharp
public string ProviderName { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Message**

Gets the exception message.

```csharp
public string Message { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **TargetSite**

```csharp
public MethodBase TargetSite { get; }
```

#### Property Value

[MethodBase](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.methodbase)<br>

### **Data**

```csharp
public IDictionary Data { get; }
```

#### Property Value

[IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.idictionary)<br>

### **InnerException**

```csharp
public Exception InnerException { get; }
```

#### Property Value

[Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)<br>

### **HelpLink**

```csharp
public string HelpLink { get; set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Source**

```csharp
public string Source { get; set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **HResult**

```csharp
public int HResult { get; set; }
```

#### Property Value

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)<br>

### **StackTrace**

```csharp
public string StackTrace { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

## Constructors

### **PackageProviderNotFoundException()**

Instantiates the `PackageProviderNotFoundException` class.

```csharp
public PackageProviderNotFoundException()
```

### **PackageProviderNotFoundException(String)**

Instantiates the `PackageProviderNotFoundException` class.

```csharp
public PackageProviderNotFoundException(string providerName)
```

#### Parameters

`providerName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the provider name.

### **PackageProviderNotFoundException(String, String)**

Instantiates the `PackageProviderNotFoundException` class.

```csharp
public PackageProviderNotFoundException(string providerName, string message)
```

#### Parameters

`providerName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the provider name.

`message` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the message.

### **PackageProviderNotFoundException(String, Exception)**

Instantiates the `PackageProviderNotFoundException` class.

```csharp
public PackageProviderNotFoundException(string message, Exception innerException)
```

#### Parameters

`message` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the message.

`innerException` [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)<br>
Specifies the inner exception.

## Methods

### **GetObjectData(SerializationInfo, StreamingContext)**

Deserializes the properties.

```csharp
public void GetObjectData(SerializationInfo info, StreamingContext context)
```

#### Parameters

`info` [SerializationInfo](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo)<br>
Serialized info.

`context` [StreamingContext](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext)<br>
Streaming context.
