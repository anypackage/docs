# GetPackageProviderCommand

Namespace: AnyPackage.Commands

The Get-PackageProvider command.

```csharp
public sealed class GetPackageProviderCommand : System.Management.Automation.PSCmdlet
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → InternalCommand → Cmdlet → PSCmdlet → [GetPackageProviderCommand](./anypackage.commands.getpackageprovidercommand.md)

## Properties

### **Name**

Gets or sets the provider name(s).

```csharp
public String[] Name { get; set; }
```

#### Property Value

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **ListAvailable**

Gets or sets if available providers are returned.

```csharp
public SwitchParameter ListAvailable { get; set; }
```

#### Property Value

SwitchParameter<br>

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

## Constructors

### **GetPackageProviderCommand()**

```csharp
public GetPackageProviderCommand()
```

## Methods

### **BeginProcessing()**

Initializes the command.

```csharp
protected void BeginProcessing()
```

### **ProcessRecord()**

Processes input.

```csharp
protected void ProcessRecord()
```
