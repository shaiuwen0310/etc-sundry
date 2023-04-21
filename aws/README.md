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

### 使用terraform建立的ec2 profile，有時候在terraform destroy時會沒刪除profile，所以只好手動刪除
* https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_manage_delete.html#id_roles_manage_delete_slr
```sh
aws iam delete-instance-profile --instance-profile-name instance-profile-name
```
