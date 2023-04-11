# ISavePackage

Namespace: AnyPackage.Provider

Interface to support `Save-Package` command.

```csharp
public interface ISavePackage
```

## Methods

### **SavePackage(PackageRequest)**

Saves packages with the specified request.

```csharp
void SavePackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
