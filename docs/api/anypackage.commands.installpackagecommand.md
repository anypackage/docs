# InstallPackageCommand

Namespace: AnyPackage.Commands

The Install-Package command.

```csharp
public sealed class InstallPackageCommand : AnyPackage.Commands.Internal.PackageCommandBase, System.Management.Automation.IDynamicParameters
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → InternalCommand → Cmdlet → PSCmdlet → [CommandBase](./anypackage.commands.internal.commandbase.md) → [PackageCommandBase](./anypackage.commands.internal.packagecommandbase.md) → [InstallPackageCommand](./anypackage.commands.installpackagecommand.md)<br>
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

### **Source**

Gets or sets the source.

```csharp
public string Source { get; set; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Prerelease**

Gets or sets if prerelease versions should be included.

```csharp
public SwitchParameter Prerelease { get; set; }
```

#### Property Value

SwitchParameter<br>

### **PassThru**

Gets or sets if the command should pass objects through.

```csharp
public SwitchParameter PassThru { get; set; }
```

#### Property Value

SwitchParameter<br>

### **TrustSource**

Gets or sets an untrusted source to trusted for this execution.

```csharp
public SwitchParameter TrustSource { get; set; }
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

### **Path**

Gets or sets the package path(s).

```csharp
public String[] Path { get; set; }
```

#### Property Value

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **LiteralPath**

Gets or sets the package path(s).

```csharp
public String[] LiteralPath { get; set; }
```

#### Property Value

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **Uri**

Gets or sets the package Uri(s).

```csharp
public Uri[] Uri { get; set; }
```

#### Property Value

Uri[]<br>

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

### **InstallPackageCommand()**

Instantiates the `InstallPackageCommand` class.

```csharp
public InstallPackageCommand()
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
