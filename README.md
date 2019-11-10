# conteco.controlplane.conteco

The _controlplane.conteco_ image of the __ContEco__ container ecosystem.

## Image Structure

This image sets the API framework for the _controlplane_ images and provides the base implementation of the API methods.  

It implements the `controlplane.conteco` interface. It inherits from `controlplane.base` internally.  
This interface is hierarchical: it implements top level methods representing life cycle stages and system areas, each with a set of submethods.

## External and Internal APIs

[`controlplane.conteco` External API](./docs/CONTROLPLANE-CONTECO-EXTERNAL-API.md)  
This API consists of two parts: the lifecycle groupings and the auxiliary groupings.  
The lifecycle groupings are common to all `controlplane` images although all methods may not be implemented.
The `controlplane.base` image provides the base implementation for this API.  
The auxiliary groupings are only implemented by `controlplane.base` and provide direct access to the different functional components.

[`controlplane.conteco` Internal API](./docs/CONTROLPLANE-BASE-CONTECO-API.md)  
This internal API contains wrappers around the various functional components.
