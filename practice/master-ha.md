# Master节点高可用

经过部署Kubernetes集群章节我们已经可以顺利的部署一个集群用于开发和测试，但是要应用到生产就就不得不考虑master节点的高可用问题，因为现在我们的master节点上的几个服务`kube-apiserver`、`kube-scheduler`和`kube-controller-manager`都是单点的而且都位于同一个节点上，一旦master节点宕机，虽然不应答当前正在运行的应用，将导致kubernetes集群无法变更。本文将引导你创建一个高可用的master节点。