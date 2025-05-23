# Adobe .NET Mobile Binding Libraries

This repository provides .NET for Android binding libraries for integrating Adobe Experience Platform (AEP) SDKs into .NET-based Android applications.

## Overview

The repository includes bindings for the following Adobe SDKs:

- **Adobe.ACPCore.Droid**
- **Adobe.ACPAnalytics.Droid**
- **Adobe.ACPIdentity.Droid**
- **Adobe.ACPLifecycle.Droid**
- **Adobe.ACPTarget.Droid**
- **Adobe.AEPAssurance.Droid**

Each binding project wraps the corresponding Adobe AAR (Android Archive) library, making it compatible with .NET for Android projects.

### Original Native SDKs

These bindings are based on the official Adobe Android SDKs:

- **Core, Identity, Lifecycle**: [github.com/adobe/aepsdk-core-android](https://github.com/adobe/aepsdk-core-android)
- **Analytics**: [github.com/adobe/aepsdk-analytics-android](https://github.com/adobe/aepsdk-analytics-android)
- **Target**: [github.com/adobe/aepsdk-target-android](https://github.com/adobe/aepsdk-target-android)
- **Assurance**: [github.com/adobe/aepsdk-assurance-android](https://github.com/adobe/aepsdk-assurance-android)

## Usage

After building, reference the generated DLLs in your .NET for Android project. Then register the desired Adobe SDK extensions like this:

```csharp
using Com.Adobe.Marketing.Mobile;
using Java.Util;

...

ACPCore.RegisterExtensions(
    new List<Class>
    {
        AEPAssurance.Extension,
        ACPAnalytics.Extension,
        ACPIdentity.Extension,
        ACPLifecycle.Extension,
        ACPTarget.Extension
    }
);

```

## License

This project is licensed under the [Apache License 2.0](LICENSE).

