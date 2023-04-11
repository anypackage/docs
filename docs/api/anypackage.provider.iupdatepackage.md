# IUpdatePackage

Namespace: AnyPackage.Provider

Interface to support `Update-Package` command.

```csharp
public interface IUpdatePackage
```

## Methods

### **UpdatePackage(PackageRequest)**

Updates packages with the specified request.

```csharp
void UpdatePackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
