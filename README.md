
My cluster

![hw12_my cluster](https://user-images.githubusercontent.com/105345932/216848598-90adf86a-2bbc-4bda-9e3a-8fa193edbca6.png)

Public IP address of worker node - 104.155.83.112

1. Information about worker node "hw12-node" saved into file workernode.txt

```echo "$(kubectl describe node hw12-node) > workernode.txt```

2. Create my namespace

![hw12-ns](https://user-images.githubusercontent.com/105345932/216852602-8ab734e9-f4cb-41a3-815f-ca4f6508a3bb.png)

3. Prepare pod-deployment.yaml file which will create a Deployment with 3 pods of Nginx server and service for access to these pods via ClusterIP and NodePort. 

![deploy and service created](https://user-images.githubusercontent.com/105345932/217067934-c246703d-1a46-4654-98c2-197fe5ae5a9e.png)

4. Show the status of deployment, pods and services. Describe all created resources and logs from pods

![2 info about depl pods svc](https://user-images.githubusercontent.com/105345932/217068458-4fd49675-394d-4d73-b406-d13f0aaddce7.png)





