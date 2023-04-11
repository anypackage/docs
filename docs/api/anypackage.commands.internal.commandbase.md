---
parent: API
---

# CommandBase

Namespace: AnyPackage.Commands.Internal

The base class for package and source commands.

```csharp
public abstract class CommandBase : System.Management.Automation.PSCmdlet, System.Management.Automation.IDynamicParameters
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → InternalCommand → Cmdlet → PSCmdlet → [CommandBase](./anypackage.commands.internal.commandbase.md)<br>
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

### **GetDynamicParameters()**

Returns an instance of an object that defines dynamic parameters.

```csharp
public object GetDynamicParameters()
```

#### Returns

[Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

            This method should return an object with properties with parameter attributes or a RuntimeDefinedParameterDictionary.

### **BeginProcessing()**

Initializes the command.

```csharp
protected void BeginProcessing()
```

### **GetInstances(String)**

Returns instances of a package provider.

```csharp
protected IEnumerable<PackageProvider> GetInstances(string provider)
```

#### Parameters

`provider` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>
Package provider name.

#### Returns

[IEnumerable&lt;PackageProvider&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>

            Returns instances of a package provider.
