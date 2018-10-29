### Usage

#### This branch (nfs) doesn't rely on any cloud provider

This means that we need nfs (for persistant volumes, see nfs-pv-pvc.yaml)

Also, we need an ingress controller in the cluster (see below)

Lastly, if we want to deploy to a master we need a DNS entry for the host that the cluster can reach (see dns-hack.yml)

#### Installation:

First, setup an ingress controller as described here: https://github.com/nginxinc/kubernetes-ingress/blob/master/docs/installation.md
**note ingress controllers only work in the namespace they run in, so change the namespace to 'pfi'

Put this in a kubernetes cluster by cloning the project.

From the project directory first run `kubectl create namespace pfi`

and then run `kubectl create -R -f .`
