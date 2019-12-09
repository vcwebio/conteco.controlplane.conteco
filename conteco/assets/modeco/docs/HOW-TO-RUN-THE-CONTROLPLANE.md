[`Back to Module`](../README.md) >> [`How To`](../docs/HOW-TO.md) >> How To Run the Controlplane

-----
The How To pages are system managed and updated whenever the base module is updated by `conteco deploy repo`.

# How to Run the Controlplane

The controlplane for module images is `vcwebio/conteco.controlplane.modeco`.  
The controlplane expects the repository to reside in the following folder structure (base module):  
`[working folder]/[realm]/modeco.${MODECO_NAME}.base`  
The `realm` can be an account (GitHub or DockerHub), or the name used to start the controlplane with.

Assuming the standard working folder for conteco `/conteco/pwd`, the mode __elk.base__ module repository of __vcwebio__  must be in `/conteco/pwd/vcwebio/modeco.elk.base`.

The reason for this is that the controlplane typically operates over multiple repositories identified by their image __type__ and __name__ and prefixed with __realm__ (account) and __ecosystem__.

## Extract Controlplane Commandline Assets

Run:

```bash
# linux
docker run -v $(pwd):/conteco/pwd vcwebio/conteco.controlplane.modeco --interactive boot-commandline linux # optional: sudo

# Windows
docker run -v %cd%:/conteco/pwd vcwebio/conteco.controlplane.modeco --interactive boot-commandline windows
```

![boot-commandline](./boot-commandline.PNG "boot-commandline")

-----
[`Back to Module`](../README.md) >> [`How To`](../docs/HOW-TO.md) >> How To Run the Controlplane
