#deploying deployment file

kubectl apply -f deployment.yaml

kubectl get deploy

kubectl get pods

kubectl describe pod <container_name>

you will get ip of the container, copy that ip of container


		# checking pod container target port working or not
			
		minikube ssh

		curl -L container_ip:3000

		exit from minikube

#deploying service

kubectl apply -f service.yaml

kubectl get svc

minikube service my-service --url

curl -L <svc_url>



# deploy ingress

kubectl apply -f ingress_k.yaml

# get ip of node

kubectl get nodes -o wide

# get svc host port, 
 
kubectl get svc   

# accesss the ingress url

curl -L <node_ip>:<target port of svc>



############### deleting environment ####################

kubectl get ingress

kubectl delete ingress name_ingress

#get svc and deployment details to delete the same

kubectl get svc

#note the name of service

kubectl delete svc <service_name>

#check service got deleted or not with get svc

kubectl get deploy
#note the name of deployment 

kubectl delete deploy <deployment_name>
#check deployment and pods and container are deleted or not


