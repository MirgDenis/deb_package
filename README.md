# DEB package module
Module that installs deb package from remote link.

# Configuration example

Example of `HostOSConfiguration` with the `deb_package` module 1.0.0 for installation of a package from provided link:

```
    apiVersion: kaas.mirantis.com/v1alpha1
    kind: HostOSConfiguration
    metadata:
      name: foo_package
      namespace: default
    spec:
      configs:
        - module: deb_package
          moduleVersion: 1.0.0
          values:
            packages:
            - link: https://<LINK_TO_DEB_PACKAGE>
      machineSelector:
        matchLabels:
          day2-custom-label: "true"
```
