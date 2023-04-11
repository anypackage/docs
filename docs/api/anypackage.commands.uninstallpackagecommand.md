---
parent: API
---

# UninstallPackageCommand

Namespace: AnyPackage.Commands

The Uninstall-Package command.

```csharp
public sealed class UninstallPackageCommand : AnyPackage.Commands.Internal.PackageCommandBase, System.Management.Automation.IDynamicParameters
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → InternalCommand → Cmdlet → PSCmdlet → [CommandBase](./anypackage.commands.internal.commandbase.md) → [PackageCommandBase](./anypackage.commands.internal.packagecommandbase.md) → [UninstallPackageCommand](./anypackage.commands.uninstallpackagecommand.md)<br>
Implements IDynamicParameters

## Properties

### **Name**

Gets or sets the name(s).

```csharp
public String[] Name { get; set; }
```

#### Property Value

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Version**

Gets or sets the version of the packages to retrieve.

```csharp
public PackageVersionRange Version { get; set; }
```

#### Property Value

[PackageVersionRange](./anypackage.provider.packageversionrange.md)<br>

**Remarks:**

Accepts NuGet version range syntax.

### **PassThru**

Gets or sets if the command should pass objects through.

```csharp
public SwitchParameter PassThru { get; set; }
```

#### Property Value

SwitchParameter<br>

### **Provider**

Gets or sets the provider.

```csharp
public string Provider { get; set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **InputObject**

Gets or sets package(s).

```csharp
public PackageInfo[] InputObject { get; set; }
```

#### Property Value

[PackageInfo[]](./anypackage.provider.packageinfo.md)<br>

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

### **UninstallPackageCommand()**

Instantiates the `UninstallPackageCommand` class.

```csharp
public UninstallPackageCommand()
```

## Methods

### **ProcessRecord()**

Processes input.

```csharp
protected void ProcessRecord()
```

### **SetRequest()**

Sets the request property.

```csharp
protected void SetRequest()
```
