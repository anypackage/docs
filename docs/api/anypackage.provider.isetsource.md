---
parent: API
---

# ISetSource

Namespace: AnyPackage.Provider

Interface to support user defined repositories and commands:
 `Set-PackageSource`, `Register-PackageSource`,
 `Unregister-PackageSource` command.

```csharp
public interface ISetSource
```

## Methods

### **RegisterSource(SourceRequest)**

Gets package sources with the specified request.

```csharp
void RegisterSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>
Package request.

### **SetSource(SourceRequest)**

Sets package sources with the specified request.

```csharp
void SetSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>
Package request.

**Remarks:**

If the requested source is not found, no exception should be thrown.

### **UnregisterSource(SourceRequest)**

Unregister a package source with the specified request.

```csharp
void UnregisterSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>
Package request.

**Remarks:**

If the requested source is not found, no exception should be thrown.
