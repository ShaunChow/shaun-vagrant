
helm install nfs-client-provisioner stable/nfs-client-provisioner -n nfs-client-provisioner --set nfs.server=172.17.8.1,nfs.path=/Users/srv/nfs/kubedata/1.15.2,storageClass.defaultClass=true,storageClass.provisionerName=nfs.shaun.io


helm install postgresql stable/postgresql -n postgresql --set postgresqlPassword=abc123


helm install keycloak codecentric/keycloak -n keycloak --set keycloak.persistence.dbVendor=postgres,keycloak.persistence.dbHost=postgresql.postgresql.svc.cluster.local,keycloak.persistence.dbUser=postgres,keycloak.persistence.dbPassword=abc123,keycloak.password=abc123,keycloak.extraVolumeMounts
helm install keycloak codecentric/keycloak -n keycloak -f ../helm3-init.yaml

helm install mysql stable/mysql -n mysql --set mysqlRootPassword=abc123,mysqlUser=mysql,mysqlPassword=abc123,mysqlDatabase=keycloak
    

helm install kubernetes-dashboard stable/kubernetes-dashboard -n kubernetes-dashboard --set image.repository=registry.cn-hangzhou.aliyuncs.com/google_containers/kubernetes-dashboard-amd64,rbac.clusterAdminRole=true


helm install metrics-server stable/metrics-server -n metrics-server


helm install metallb stable/metallb -n metallb