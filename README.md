##commands

   10  kubectl get pods --namespace kube-system
   11  kubectl nodes
   12  kubectl get nodes
   13  kubectl get namespaces
   14  ls
   15  vi namespace.yaml
   16  kubectl apply -f namespace.yaml
   17  kubectl get namespaces
   18  kubectl get nodes
   19  kubectl get pods --namespace kube-system
   20  kubectl get namespace
   21  ls
   22  kubectl delete -f namespace.yaml
   23  clear
   24  kubectl get namespace
   25  vi namespace.yaml
   26  kubectl apply -f namespace.yaml
   27  kubectl get namespace
   28  kubectl config get-contexts
   29  kubectl config set-context dev --namespace=development --cluster=kubernetes --user=kubernetes-admin
   30  kubectl config get-contexts
   31  kubectl config use-context dev
   32  kubectl config get-contexts

vi resourceLimits.yml
   39  vi resoureQuota.yml
   40  kubectl get namespace
   41  kubectl get namespace -o wide
   42  kubectl describe namespace development
   43  kubectl apply -f resoureQuota.yml
   44  vi resoureQuota.yml
   45  kubectl apply -f resoureQuota.yml
   46  kubectl describe namespace development
   47  vi resourceLimits.yml
   48  ls
   49  vi LimitRange.yaml
   50  kubectl apply -f LimitRange.yaml --namespace development
   51  kubectl describe namespace development
   52  vi pod.yaml
   53  kubectl apply -f pod.yaml
   54  vi LimitRange.yaml
   55  kubectl apply -f LimitRange.yaml --namespace development
   56  vi LimitRange.yaml
   57  kubectl apply -f LimitRange.yaml --namespace development
   58  kubectl -f delete LimitRange.yaml
   59  kubectl delete -f LimitRange.yaml
   60  kubectl describe namespace development
   61  kubectl apply -f pod.yaml
   62  vi resourceLimits.yml
   63  vi pod.yaml
   64  kubectl apply -f pod.yaml
   65  vi pod.yaml \
   66  vi pod.yaml
   67  kubectl apply -f pod.yaml
   68  kubectl describe namespace development
   69  kubectl get ppods
   70  kubectl get pods
   71  kubectl get pods -o wide
   72  kubectl describe pod sample-pod
   73  kubectl get pods
   74  kubectl delete pod sample-pod
   75  kubectl get pods


---------------------------------------------------------------------------------------------------------------------------------------------------

Docker Creation
1.sudo -i
2. sudo apt update
3. sudo apt install -y docker.io
4. systemctl start docker
5. systemctl enable docker
6.systemctl status docker




linking containers:
For two container to talk to each other -
its legacy feature


1) docker container ls

remove any existing containers

2) docker container run -d -p 24000:80 --name apache-2 httpd:latest

3) docker container run -d -p 25000:80 --name apache-3 --link apache-2 httpd:latest

how to verify ?

go inside the container

4) docker container exec -it apache-3 /bin/bash

5)hostname

6) ping apache-2

7) apt-get update > /dev/null

8) apt-get install -y iputils-ping >/dev/null


9) ping apache-2
