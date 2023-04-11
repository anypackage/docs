# PackageSourceNotFoundException

Namespace: AnyPackage.Provider

The `PackageSourceNotFoundException` class.

```csharp
public class PackageSourceNotFoundException : PackageProviderException, System.Runtime.Serialization.ISerializable
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) → [PackageProviderException](./anypackage.provider.packageproviderexception.md) → [PackageSourceNotFoundException](./anypackage.provider.packagesourcenotfoundexception.md)<br>
Implements [ISerializable](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.serialization.iserializable)

## Properties

### **SourceName**

Gets the source name.

```csharp
public string SourceName { get; }
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

### **PackageSourceNotFoundException()**

Instantiates the `PackageSourceNotFoundException` class.

```csharp
public PackageSourceNotFoundException()
```

### **PackageSourceNotFoundException(String)**

Instantiates the `PackageSourceNotFoundException` class.

```csharp
public PackageSourceNotFoundException(string sourceName)
```

#### Parameters

`sourceName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the source name.

### **PackageSourceNotFoundException(String, String)**

Instantiates the `PackageSourceNotFoundException` class.

```csharp
public PackageSourceNotFoundException(string sourceName, string message)
```

#### Parameters

`sourceName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the source name.

`message` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Specifies the message.

### **PackageSourceNotFoundException(String, Exception)**

Instantiates the `PackageSourceNotFoundException` class.

```csharp
public PackageSourceNotFoundException(string message, Exception innerException)
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
