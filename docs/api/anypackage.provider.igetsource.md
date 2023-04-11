---
parent: API
---

# IGetSource

Namespace: AnyPackage.Provider

Interface to support `Get-PackageSource` command.

```csharp
public interface IGetSource
```

## Methods

### **GetSource(SourceRequest)**

Gets package sources with the specified request.

```csharp
void GetSource(SourceRequest request)
```

#### Parameters

`request` [SourceRequest](./anypackage.provider.sourcerequest.md)<br>
Package request.

**Remarks:**

If the requested source is not found, no exception should be thrown.
