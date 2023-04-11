# IUninstallPackage

Namespace: AnyPackage.Provider

Interface to support `Uninstall-Package` command.

```csharp
public interface IUninstallPackage
```

## Methods

### **UninstallPackage(PackageRequest)**

Uninstalls packages with the specified request.

```csharp
void UninstallPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
