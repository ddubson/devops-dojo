# Creating a Pod

To create a simple pod in Kubernetes, you will need a pod definition
file (which can either be JSON or YAML).

`simple_pod.yaml` is a sample definition file that can be used to create an nginx pod on a kubernetes cluster.

To create the pod, run:
`kubectl create -f single_pod.yaml`

To check if the pod has been created successfully, run:
`kubectl get pods`

To get a detailed description of the pod and its running state, run:
`kubectl describe pod nginx-pod`
