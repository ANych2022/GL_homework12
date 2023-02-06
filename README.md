
My cluster

![hw12_my cluster](https://user-images.githubusercontent.com/105345932/216848598-90adf86a-2bbc-4bda-9e3a-8fa193edbca6.png)

Public IP address of worker node - 104.155.83.112

1. Information about worker node "hw12-node" saved into file workernode.txt

```echo "$(kubectl describe node hw12-node) > workernode.txt```

2. Create my namespace

![hw12-ns](https://user-images.githubusercontent.com/105345932/216852602-8ab734e9-f4cb-41a3-815f-ca4f6508a3bb.png)

3. Prepare pod-deployment.yaml file which will create a Deployment with 3 pods of Nginx server and service for access to these pods via ClusterIP and NodePort. 

![deploy and service created](https://user-images.githubusercontent.com/105345932/217067934-c246703d-1a46-4654-98c2-197fe5ae5a9e.png)

4. Show the status of deployment, pods and services. 

![21 info about depl pods svc](https://user-images.githubusercontent.com/105345932/217071599-fed9e5c5-e808-41ba-90e8-e0f724018c0d.png)

5. Describe all created resources and show logs from pods:
 - description of the deployment
 
 ![3 deploy description](https://user-images.githubusercontent.com/105345932/217073702-a54d86b9-465a-4d36-ab03-6ca6b1ab6cb3.png)
 
 - description of the pod
 
 ![5 describe pod](https://user-images.githubusercontent.com/105345932/217074106-f608a76b-6677-426f-9e3c-42cde9c6c9b0.png)
 
 - description of the services

![41 svc description](https://user-images.githubusercontent.com/105345932/217079502-34a21d81-d605-4b42-87ba-27268aea5982.png)

- log of the pod

![6 pod log](https://user-images.githubusercontent.com/105345932/217081423-22c7a26c-2aa5-4fb6-950b-24dfadfed4a0.png)

6. Prepare two job yaml files:
 - one gets content via curl from an internal port (ClusterIP) - curl-clusterip.yaml
 - second, get content via curl from an external port (NodePort) - curl-nodeport.yaml
 
 ![7 create jobs](https://user-images.githubusercontent.com/105345932/217096102-f5d1360a-139a-48c5-bc3a-876386523f38.png)
  
  Check logs for each job:
  
  ![8 logs cluster ip](https://user-images.githubusercontent.com/105345932/217097927-36f1974e-1eb1-4a2e-a7e8-b044e40343f1.png)
  
  ![9 logs nodeport](https://user-images.githubusercontent.com/105345932/217097963-a8c80105-98b3-42a3-9b9f-4bdce9134310.png)

7. Prepare cronjob.yaml file which will test the connection to Nginx or Apache service every 3 minutes.

![10 apply cronjob](https://user-images.githubusercontent.com/105345932/217098318-73bc71e3-a574-4652-8feb-42cadff2a5df.png)

 - describe cronjob

![11 decribe cj](https://user-images.githubusercontent.com/105345932/217098526-2df9f207-39f8-4ce4-9b5e-265c9bc97d24.png)

- list cronjobs

![12 cj test](https://user-images.githubusercontent.com/105345932/217098676-8e001996-7fa2-42d1-b5b1-0994ae88bf7c.png)

- log of one cronjob

![14 status cj](https://user-images.githubusercontent.com/105345932/217103917-e28d919c-900c-41eb-bfd8-f73595c2c259.png)




















