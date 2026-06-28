First, perform a git clone of the repository https://github.com/docker-archive/swarm-microservice-demo-v1. After that, check the Dockerfiles located in the vote worker and vote app directories. Once you have reviewed the Dockerfiles there, check whether those images exist on Docker Hub. If they do not exist on Docker Hub, build and push the Docker images yourself.

Next, configure the YAML files for the components—such as the database (db), result (result), worker (worker), and vote (vote)—along with their required ports. Before carrying out these steps, ensure that you have set up a Kubernetes cluster using Google Kubernetes Engine (GKE) via Terraform. This includes the creation of the Kubernetes cluster along with the networking and other necessary configurations.


- git clone https://github.com/adamshaffa/test-case.git

- code test-case or cd test-case





### before running terraform u must : 
- run gcloud auth login for gcp


## To Run Terraform 

- Open the main.tf 
- change project to your project name ( in this case i use GCP. If use AWS or ETC Change to the resource )
- run terraform init
- run terraform apply

## Run the app 
kubectl create -f k8s-specifications/

## To remove them, run:


kubectl delete -f k8s-specifications/

## TO see 

It must be on http://"localhost":31000 for the vote
It must be on http://"localhost":31000 for the view
