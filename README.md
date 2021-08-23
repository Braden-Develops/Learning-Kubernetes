Setting up Kubernetes on my Raspberry Pi cluster.
https://ubuntu.com/tutorials/how-to-kubernetes-cluster-on-raspberry-pi#1-overview

Ansible to reduce the pain of setting up 4 nodes.

Presupposes some knowledge of Docker and you must have a Docker Hub account for repo pulls
In my case I learned all I needed to know by accidentally hitting the 'Docker Images: Build Image' button in VSCode.

docker container [ls, rm]
docker image [ls, rm]
docker build [-t repo/name:tag] .
docker tag $image} repo/name:tag
docker push repo/name:tag
docker pull repo/name:tag
docker run repo/name:tag
docker stop repo/name:tag

Installing KubeCtl
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

Configure KubeCtl to target remote machine.
(Copy config from masternode and place on desired system, WSL in my case. Then edit the file and change the 127.0.0.1 reference to the IP of your parent node.)
kubectl get pods -v=6 to find path to config file if it is not in your home

kubectl get pods
kubectl get deployments
microk8s.kubectl

Create Docker secret https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/

Create Kubernetes deployment
https://youtu.be/nn9J9sWLj_w

DNS Woes with Kubernetes pods
https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/#what-things-get-dns-names

Python woes? chmod +x in DockerFile and shebang in main script

Still need to figure out inter-pod DNS!

What's next?