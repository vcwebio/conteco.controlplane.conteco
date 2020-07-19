[`controlplane.conteco`](../README.md) >> API Auxiliary Methods

-----

# API Auxiliary Methods

## `/conteco/bin`

__`conteco`__  
Entrypoint for the API when called from the CLI.

## `/conteco/bin/controlplane/internal`

__`.conteco`__  
Entrypoint for the API if called as a base API from a derived controlplane.

## `/conteco/bin/controlplane/conteco/internal`

This folder contains auxiliary methods supporting the implementation of the `config` API.

__`config-deploy-gather-stacks-module`__  
Copies the stack docker-compose.yml files and creates the module _environment.template_ settings base file.  
Used by CONTECO_TYPE _module_ only.

__`config-deploy-generate-docker-compose-yml`__  
Generates the docker-compose.yml file applying the environment variables in the CONTECO_DC_GLOBAL list.  
This is the final step for docker-compose.yml.

__`config-deploy-generate-environment-module`__  
Generates the _environment.module_ settings file used when creating / updating the ModEco modules.  
This groups the settings per type groups across all stacks.

__`config-deploy-generate-environment-stack`__  
Generates the _environment_ settings type for the stack and module CONTECO_TYPE.

__`config-deploy-generate-templates-stack`__  
Generates the _docker-compose.yml.template_ and _environment.template_ file for the CONTECO_TYPE stack type.

__`deploy-up`__  
Generates the actual docker-compose.yml file applying the _environment_ non global settings and starts the service stack.

-----
[`controlplane.conteco`](../README.md) >> Auxiliary API
