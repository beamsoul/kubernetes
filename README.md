![Create Kubernetes YAML for Deployment, Service](https://user-images.githubusercontent.com/50894237/60642231-05632a00-9de4-11e9-9bd2-397561885c42.jpg)
# kubernetes
A Kubernetes pod is a group of containers that are deployed together on the same host. If you frequently deploy single containers, you can generally replace the word "pod" with "container" and accurately understand the concept.
here some examples what we have covered in April class Projects 

# benchmarker-ds.yaml

here some steps for deployment 

Vim benchmarker-ds.yaml

git add .


git commit -a -m "it creates one pod in each nodes"

git push origin master

kubectl create -f benchmarker-ds.yaml

ubectl get daemonsets

kubectl get ds

kubectl pods -o wide | grep brenchmarker


kubectl expose daemonset benchmarker-ds --type=NodePort

kubectl expose daemonset benchmarker-ds-zbnzn --type=NodePort

kubectl expose pods benchmarker-ds-zbnzn --type=NodePort

kubectl get services  (this is the last step when we can test it, we can use external ip by giving a command kubectl pods -o wide to see all internal and external IPS

KUARD-RS-TEST.YAML
kubectl create -f kuard-rs-test.yaml
 
   
   git pull origin master
   
  kubectl create -f kuard-rs-test.yaml
  
  kubectl get rs
  
  kubectl autoscale rs kuard-rs-test --name=kuard-rs-test-hpa --min=2 --max=20 --cpu-percent=50
  
  kubectl get hpa
  
  kubectl expose rs kuard-rs-test.yaml --type=NodePort

kubectl get nodes -wide
 
kubectl get nodes -o wide

 kubectl get services
 
  kubectl get pods
  
   kubectl top pods
   
 DEPENDING ON MY CPU USAGE 

