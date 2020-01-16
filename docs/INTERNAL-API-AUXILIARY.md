[`controlplane.base`](../README.md) >> API Auxiliary Methods

-----

# API Auxiliary Methods

## `/conteco/bin`

__`base`__  
Entrypoint for the API when called from the CLI.

## `/conteco/bin/controlplane/internal`

__`.base`__  
Entrypoint for the API if called as a base API from a derived controlplane.

## `/conteco/bin/controlplane/base/internal`

This folder contains auxiliary methods supporting the implementation of the `config` API.

__`config-increment-version`__ [$versionpart] [$rootpath]  
Auxiliary method that takes the `$CONTECO_TAG` variable and increments the requested version part (_major_, _minor_ or _revision_).
It updates the version by calling the `config-set-version` auxiliary method.  
It only operates on the version format `vx.y.z`.

__`config-remove-crs`__  
Auxiliary method that remove CRs from files with no extension, `.static` or `.md` extension in selected folders.

__`config-set-version`__ [$version] [$rootpath]  
Sets the new version in the `$CONTECO_TAG` variable and `environment` file.

-----
[`controlplane.base`](../README.md) >> Auxiliary API
