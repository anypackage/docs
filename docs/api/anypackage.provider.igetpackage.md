# IGetPackage

Namespace: AnyPackage.Provider

Interface to support `Get-Package` command.

```csharp
public interface IGetPackage
```

## Methods

### **GetPackage(PackageRequest)**

Gets packages with the specified request.

```csharp
void GetPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
