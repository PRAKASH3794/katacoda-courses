Fill your cluster will some Pods. First, add a few simple NGINX Pods to the default namespace.

`kubectl create -f nginx.yaml`{{execute}}

Next, add a few more Pods to a second namespace.

`kubectl create namespace more-apps`{{execute}}

`kubectl create --namespace more-apps -f ghost.yaml`{{execute}}

The Deployments and Pods are labeled to both mark these Pods a potential victim targets of the Chaoskube Pod killer. They are also labeled for easy observability. See the labels applied to the deployment and Pod template.

`ccat nginx.yaml`{{execute}}

The deployment and Pod template have the label `app-purpose: chaos` which make the Pod an eligible target for Chaoskube since that was the label target provided as a configuration value in the Helm chart installation.

In the next step, observe the running containers and how they are randomly disrupted.
