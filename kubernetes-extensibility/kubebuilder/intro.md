# Creating and Operator based on Kubebuilder #

<img align="right" src="/javajon/courses/kubernetes-extensibility/kubebuilder/assets/kubebuilder.png" width="300">

This scenario lets you experience developing an Operator with Kubebuilder. You will create a CRD through Golang structs and automation. You will see how RBACs are created through generation from code annotations. Then you will create a controller for working with the CRD.

This lab and code was inspired by the previous work of [cnat](https://github.com/programming-kubernetes/cnat) (cloud native at akin to Linux at command) and an outdated tutorial on [Kuberbuilder with cnat](https://github.com/programming-kubernetes/cnat/tree/master/cnat-kubebuilder). That code is out of date for the current versions of controller-runtime and Kubebuilder. Using it as a reference you will notice some nice improvements to standard patterns in controller-runtime.

The basics of this operator is that we will have an at CRD which takes a time and command. A controller will monitor the CRD and Pods. The controller will create at kinds and will create a pod to run the command if the time has past. Once the pod is finished running, the controller will update the CR regarding the pod status.

## Kuberbuilder ##

Kubebuilder is a framework for building Kubernetes APIs using [custom resource definitions (CRDs)](https://kubernetes.io/docs/tasks/access-kubernetes-api/extend-api-custom-resource-definitions).

In this scenario you will learn how to:

- todo
- todo
- todo
- todo