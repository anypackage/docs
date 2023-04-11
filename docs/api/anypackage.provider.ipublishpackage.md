---
parent: API
---

# IPublishPackage

Namespace: AnyPackage.Provider

Interface to support `Publish-Package` command.

```csharp
public interface IPublishPackage
```

## Methods

### **PublishPackage(PackageRequest)**

Publishes packages with the specified request.

```csharp
void PublishPackage(PackageRequest request)
```

#### Parameters

`request` [PackageRequest](./anypackage.provider.packagerequest.md)<br>
Package request.

**Remarks:**

If the requested package is not found, no exception should be thrown.
