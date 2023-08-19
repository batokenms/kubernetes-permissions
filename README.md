# kubernetes-permissions

# ClusterRole 

A ClusterRole is a set of rules that define a set of permissions within the entire cluster. 
These permissions determine what actions are allowed on which resources. 
ClusterRoles are not namespaced and can be used across the entire cluster.

![image](https://github.com/joshking1/kubernetes-permissions/assets/88409463/2a238df4-58ea-47d7-b367-a14b81767223)


# ClusterRoleBinding
A ClusterRoleBinding binds a ClusterRole to a user, group, or ServiceAccount within a specific namespace or 
across the entire cluster, granting the permissions defined in the ClusterRole.

![image](https://github.com/joshking1/kubernetes-permissions/assets/88409463/a4682454-1fdd-4261-ac82-ab941959ee58)

  

# ServiceAccount:
A ServiceAccount is an identity used by pods to interact with the Kubernetes API and other resources. 
ServiceAccounts are often used in conjunction with RBAC to control the permissions and access levels of pods.

![image](https://github.com/joshking1/kubernetes-permissions/assets/88409463/c4ffc82c-3f5b-427b-8315-05619f90087a)
