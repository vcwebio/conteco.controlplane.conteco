# controlplane.conteco - ContEco

The `controlplane.conteco` image of the __ContEco__ container ecosystem.
See `conteco.docs.overview` for more information on the ContEco ecosystem.

The `controlplane.conteco` image implements the controlplane for the ContEco ecosystem and is concerned with container image configuration.  
The output is a set of images that is easily composed into modules - which are managed by the ModEco controlplane.  
It provides an API for console, repo, build, release, deploy but not for run.  
Inherited from `controlplane.base`:
* console - in full, no changes
* repo - in full, no changes
* config - in full, adding extensions
* build - in full, no changes
* release - in full, no changes
Implemented or changes added to:
* deploy - full implementation

## Controlplane API

* __console__  
API section containing methods that executes outside the context of a repository.  
Inherited in full from `controlplane.base`.

* __repo__  
API section dealing with version control, GIT based or directly ported from GIT.  
Inherited in full from `controlplane.base`.

* __config__  
API section dealing with repository configuration.  
Inherits implementation from `controlplane.base` and adding further methods.  
Full implementation - [config API in detail](./docs/CONTROLPLANE-API-CONFIG.md)

* __build__
Build API - container images only.  
Inherited in full from `controlplane.base`.

* __release__  
Release API - container images only.  
Inherited in full from `controlplane.base`.

* __deploy__
Deploy API - of container images, modules or solutions.  
Full implementation - [deploy API in detail](./docs/CONTROLPLANE-API-DEPLOY.md)

* __run__
Run API - of modules or solutions.
No implementation within `controlplane.conteco`.

## `controlplane` CLI

See `conteco.docs.overview` for more information on how to extract and use the commandline interface.
