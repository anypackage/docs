# ProviderArgumentCompleter

Namespace: AnyPackage.Commands

The Provider parameter argument completer.

```csharp
public sealed class ProviderArgumentCompleter : System.Management.Automation.IArgumentCompleter
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [ProviderArgumentCompleter](./anypackage.commands.providerargumentcompleter.md)<br>
Implements IArgumentCompleter

## Constructors

### **ProviderArgumentCompleter()**

```csharp
public ProviderArgumentCompleter()
```

## Methods

### **CompleteArgument(String, String, String, CommandAst, IDictionary)**

```csharp
public IEnumerable<CompletionResult> CompleteArgument(string commandName, string parameterName, string wordToComplete, CommandAst commandAst, IDictionary fakeBoundParameters)
```

#### Parameters

`commandName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`parameterName` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`wordToComplete` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`commandAst` CommandAst<br>

`fakeBoundParameters` [IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.idictionary)<br>

#### Returns

[IEnumerable&lt;CompletionResult&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)<br>
