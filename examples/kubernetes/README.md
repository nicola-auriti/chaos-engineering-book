## Macbook M1 support notes

Minikube can simply be installed with `brew` command.

In order to initialise it, the driver to be used is QEMU: `minikube start --driver qemu --network socket_vmnet`. Refer to https://minikube.sigs.k8s.io/docs/drivers/qemu/.
Also, the setup that originally came with this example used a version of Goldpinger that didn't support ARM architectures. Updating the docker image version to https://hub.docker.com/r/bloomberg/goldpinger/tags?name=3.10
is a solution to the problem.

### Pip & Virtualenv

The instructions in the book don't work and are missing a few steps.

`virtualenv` is a module to be installed with brew, which will depend on python. The command to use in order to create a new virtual environment is `virtualenv -p python3 <ENV_NAME>`.
