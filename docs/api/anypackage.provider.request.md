# Request

Namespace: AnyPackage.Provider

Request base class used to send information to the package provider.

```csharp
public abstract class Request
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [Request](./anypackage.provider.request.md)

## Properties

### **DynamicParameters**

Gets the package provider dynamic parameters.

```csharp
public object DynamicParameters { get; internal set; }
```

#### Property Value

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

### **ParameterSetName**

Gets the parameter set name.

```csharp
public string ParameterSetName { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Stopping**

Gets if the package provider has been requested to stop.

```csharp
public bool Stopping { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **ProviderInfo**

Gets the package provider information.

```csharp
public PackageProviderInfo ProviderInfo { get; internal set; }
```

#### Property Value

[PackageProviderInfo](./anypackage.provider.packageproviderinfo.md)<br>

## Methods

### **ShouldContinue(String, String)**

```csharp
public bool ShouldContinue(string query, string caption)
```

#### Parameters

`query` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`caption` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **ShouldContinue(String, String, Boolean&, Boolean&)**

```csharp
public bool ShouldContinue(string query, string caption, Boolean& yesToAll, Boolean& noToAll)
```

#### Parameters

`query` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`caption` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`yesToAll` [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean&)<br>

`noToAll` [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean&)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **ShouldContinue(String, String, Boolean, Boolean&, Boolean&)**

```csharp
public bool ShouldContinue(string query, string caption, bool hasSecurityImpact, Boolean& yesToAll, Boolean& noToAll)
```

#### Parameters

`query` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`caption` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`hasSecurityImpact` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

`yesToAll` [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean&)<br>

`noToAll` [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean&)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **WriteDebug(String)**

Write debug information to the debug stream.

```csharp
public void WriteDebug(string text)
```

#### Parameters

`text` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Debug information.

### **WriteInformation(Object, String[])**

Route information to the user or host.

```csharp
public void WriteInformation(object messageData, String[] tags)
```

#### Parameters

`messageData` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>
The object / message data to transmit to the hosting application.

`tags` [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

            Any tags to be associated with the message data.
            These can later be used to filter or separate objects being sent to the host

### **WriteInformation(InformationRecord)**

Write information to the information stream.

```csharp
public void WriteInformation(InformationRecord informationRecord)
```

#### Parameters

`informationRecord` InformationRecord<br>
Information.

### **WriteProgress(ProgressRecord)**

Write progress information to the progress stream.

```csharp
public void WriteProgress(ProgressRecord progressRecord)
```

#### Parameters

`progressRecord` ProgressRecord<br>
Progress information.

### **WriteVerbose(String)**

Write verbose information to the verbose stream.

```csharp
public void WriteVerbose(string text)
```

#### Parameters

`text` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Verbose message.

### **WriteWarning(String)**

Write warning information to the warning stream.

```csharp
public void WriteWarning(string text)
```

#### Parameters

`text` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Warning information.
