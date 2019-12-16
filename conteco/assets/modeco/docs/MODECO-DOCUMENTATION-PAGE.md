# The Modeco Documentation image

This image contains the information about all aspects of the __modeco__ ecosystem.  

## Introduction

__Modeco__ concerns itself with the ecosystem of functional modules.  
Container images typically contain applications that can be configured to suits different purposes.  
However, more often than not does a module consists of multiple applications - i.e. containers - configured to work together.   

## What is a Module?

The concept of module exists in both __conteco__ and __modeco__ but address different concerns.  
__Conteco__ concerns itself with the structural configuration of containers featuring applications.
The end product is working module ready to be functionally configured for a specific purpose.  
The variants that exists for a specific __modeco__ module type differ in operational configuration but are functionally the same.



## Managing a Module

### How to Configure a Module

```bash
modeco config build <selector>
```
The standard build configuration command for a project in general, not __modeco__ specific.

```bash
modeco config module <selector>
```
Specific command to configure the stack `docker-compose.yml` files.  
The command needs to be executed when changes have been made to `settings.global` or when the __conteco__ structural module definition has published changes to the base repository.  

```bash
modeco config volume <selector>
```
This modele specific command backs the contents of the data volumes that need initialisation.  
It is typically executed after configuration changes have been made to the resp. applications.
Note that it is strongly advised to shudown the module first.

### How to Build a Module

```bash
modeco build <selector>
```
The standard build command to build the container image from the project settings.

### How to Release a Module

```bash
modeco release <selector>
```
The standard release command to push the container image to an image repository.

### How to Deploy a Module

```bash
modeco deploy module <selector>
```
Specific command to deploy all prerequisites in order to run the module.  
It creates the module overlay network, the data volumes and adds initialisation data to the volumes where required. 

### How to Run a Module

The `run` interface implements 6 methods: `boot`, `start`, `pause`, `resume`, `stop` and `shutdown`.
