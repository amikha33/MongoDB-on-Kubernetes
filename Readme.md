# Setting Up MongoDB

## Process to Follow installation on K8s

In Master Node :


    sudo mkdir /mnt/data
    kubectl label nodes controlplane size=large
    kubectl apply -k .
    kubectl get pod
    kubectl exec -it mongodb-test-0 -- sh
    mongo
    use test
    db.auth('test','password#@12')
