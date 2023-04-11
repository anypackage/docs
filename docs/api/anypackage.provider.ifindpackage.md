---
parent: API
---

# IFindPackage

Namespace: AnyPackage.Provider

Interface to support `Find-Package` command.

```csharp
public interface IFindPackage
```

## Methods

### **FindPackage(PackageRequest)**

Finds packages with the specified request.

```csharp
void FindPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
