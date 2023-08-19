# kubernetes-permissions

# ClusterRole 

A ClusterRole is a set of rules that define a set of permissions within the entire cluster. 
These permissions determine what actions are allowed on which resources. 
ClusterRoles are not namespaced and can be used across the entire cluster.

apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRole
metadata:
  name: example-clusterrole
rules:
- apiGroups: [""]
  resources: ["pods"]
  verbs: ["get", "list", "watch"]

# ClusterRoleBinding
A ClusterRoleBinding binds a ClusterRole to a user, group, or ServiceAccount within a specific namespace or 
across the entire cluster, granting the permissions defined in the ClusterRole.

apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: example-clusterrolebinding
subjects:
- kind: ServiceAccount
  name: default
  namespace: default
roleRef:
  kind: ClusterRole
  name: example-clusterrole
  apiGroup: rbac.authorization.k8s.io
  

# ServiceAccount:
A ServiceAccount is an identity used by pods to interact with the Kubernetes API and other resources. 
ServiceAccounts are often used in conjunction with RBAC to control the permissions and access levels of pods.

apiVersion: v1
kind: ServiceAccount
metadata:
  name: example-serviceaccount
  namespace: default
