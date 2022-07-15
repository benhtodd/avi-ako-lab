## THIS README WORKS FOR THE LIVEFIRE LABS ONLY

The AKO Values file has been highly modified for our labs. Reference AVI Documention to Make it work for your setup

In this lab you will be deploying the AVI Kubernetes Operator(AKO) using HELM. You will customize the AKO deployment to define specific tenant, cluster name, and a series of other settings, to demonstrate some of the capabilities of the AKO. You need some files to help you with these efforts.

clone the git repo

```
git clone  https://github.com/benhtodd/avi-ako-lab
```

Copy and rename the "BASE-ako-values.yaml" as a backup. 

In the new file replace the entries you see variables wrapped in < >

* Line 19: clusterName: <users_cluster_name_here> - # A unique identifier for the kubernetes cluster, that helps distinguish the objects for this cluster in the avi controller. // MUST-EDIT

* Line 73: <tenant_name_here>   # <miuser00x> Name of the tenant where all the AKO objects will be created in AVI.

* Line 97: authtoken:  '< authtokenhere >' # Get OAUTH token provided by instructor

Save this AKO Values File for use later

Install the AKO Helm Chart

Next you will need to add the repo for the AKO Helm chart to your local repo

Run

```
helm repo add ako https://projects.registry.vmware.com/chartrepo/ako
```

