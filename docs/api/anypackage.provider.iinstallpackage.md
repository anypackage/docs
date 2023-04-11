# IInstallPackage

Namespace: AnyPackage.Provider

Interface to support `Install-Package` command.

```csharp
public interface IInstallPackage
```

## Methods

### **InstallPackage(PackageRequest)**

Installs packages with the specified request.

```csharp
void InstallPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
