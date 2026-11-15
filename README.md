Set up kubectl

1) apt update

2) apt upgrade

3) apt install -y curl wget ca-certificates gnupg apt-transport-https conntrack

4) curl -fsSL https://get.docker.com -o get-docker.sh

5) sh get-docker.sh

6) systemctl status docker

7) systemctl enable docker

8) KUBECTL_VERSION=$(curl -L -s https://dl.k8s.io/release/stable.txt)

   echo $KUBECTL_VERSION
   
9) curl -LO https://dl.k8s.io/release/v1.37.2/bin/linux/amd64/kubectl  --> Replace v1.37.2 with KUBECTL_VERSION

10) install -o root -g root  -m 0755 kubectl /usr/local/bin/kubectl
    kubectl version --client
	


Install minikube

1)  Download minikube
    curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64
	
	
2) Install downloaded minikube
   sudo install minikube-linux-amd64 /usr/local/bin/minikube
   minikube version
   
3) usermod -aG docker ubuntu

4) su -ubuntu

5) minikube start --driver=docker  --container-runtime=containerd --cpus=2 --memory=4096

6) minikube status  --> Gives minikube status

7) kubectl get nodes --> List the nodes for minikube

8) kubectl get pods -A   --> get all pods

9) kubectl get pods -n kube-system        -> get pods for kube-system


<img width="940" height="301" alt="image" src="https://github.com/user-attachments/assets/bf419787-8541-402c-9605-3533509a24de" />


Build docker images


<img width="940" height="497" alt="image" src="https://github.com/user-attachments/assets/bb2ad309-c1c2-497e-a425-c6f392f9ebe0" />



Validate if services are working



<img width="940" height="99" alt="image" src="https://github.com/user-attachments/assets/58fdbcab-f982-4eef-bddb-8b469c26ba95" />


<img width="940" height="330" alt="image" src="https://github.com/user-attachments/assets/7c2bf6e7-0e68-4a1f-b1b8-bbedc6e3f17f" />


<img width="940" height="275" alt="image" src="https://github.com/user-attachments/assets/4d99e064-5980-4266-b6c0-086c6cdaa17f" />


<img width="940" height="143" alt="image" src="https://github.com/user-attachments/assets/fe126659-2979-45c8-ad78-2aa59df312fc" />



Verifying services :

<img width="1230" height="143" alt="image" src="https://github.com/user-attachments/assets/161ddc53-f583-4eda-a924-6990399c4591" />

Kubernetes logs

<img width="900" height="106" alt="image" src="https://github.com/user-attachments/assets/30425d56-9f77-4ffb-97f7-3f52bd448e4c" />













