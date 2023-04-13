# AWS
### 使其他IAM user有權限使用我建立的EKS
```
kubectl edit cm -n kube-system aws-auth
```
```
judy@JudydeMac-mini iam_user_to_eks % kubectl describe cm -n kube-system aws-auth
Name:         aws-auth
Namespace:    kube-system
Labels:       <none>
Annotations:  <none>

Data
====
mapRoles:
----
- groups:
  - system:bootstrappers
  - system:nodes
  rolearn: arn:aws:iam::123456789123:role/dev-tpd-nodegroup-role
  username: system:node:{{EC2PrivateDNSName}}
- groups:
  - system:masters
  rolearn: arn:aws:iam::123456789123:user/kane
  username: kane


BinaryData
====

Events:  <none>
```
