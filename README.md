# Pollinate-AKS

# Pollinate-AKS Create Azure AKS Cluster
*refer AKScodehelp.docx for more details:-
Overview
This repository is offered for create features with the Azure Kubernetes Service (AKS). This repository is monitored by the AKS Monitor 
Also create 2 Pod for one pod for database and second pod for web server.
Overview

AKS Cluster creates with No of Azure Components	 
Azure Resource Group name: - azure-aks-rg inside resouce group creates	 
AKS Monitor: - aksmonitor-17231297914367105045	
AKS Cluster: - az-aks-Cluster	
AKS Network: - azure-aks-rg-network	
AKS Routetable: azure-aks-rg-routetable	
AKS ContainerInsights:-ContainerInsights(aksmonitor-17231297914367105045)	

This script runs in Two Parts, First Parts: - Terraform script creates AKS, Second Parts: - Create Pod and mount Image to Pod 
(1)	First Parts use Terraform script for create AKS cluster.

Terraform script runs from your Local computer or Azure Pipeline.

Terraform scrips runs from your Local Computer then require following prerequisite tools.
1.	Azure CLI
2.	Azure Powershell
3.	Visual Studio 2019 with Kubernetes
4.	Visual Studio code
5.	Git install
6.	kubernetes-cli
7.	Terraform
8.	Docker
9.	Azure Account for Create AKS

Very easy way to installed to your local computer on Powershell (adminsrator) using choco install docker-desktop –y.
 

Go to https://github.com/ashishpatel3/Pollinate-AKS and download repository to your local computer folder.
 Then got to your folder & open Powershell.exe

Login into Azure using command az Login
 
Run command terraform init for terraform initialisation.
Terrform Code :- terraform init
 
Run command terraform plan for terraform plan
Terrform Code: - terraform plan

 
Run Terraform code apply for create aks into resource group.
Terraform code:-terraform apply  --auto-approve
 
Terraform created following resource group including aks.

 
Also Terraform code run from Azure Pipeline.
Go to Azure Devops , click on pipline create new pipeline , click on classic editor on bottom
 

Click on GitHub or import git hub repository to Azure Repository then use Azure Repos Git

 
Select Project  with branch then click on empty job
 

Then go to agent job and search terraform
 
Create Terraform 3 job
Terraform Init
Terraform plan
Terraform apply




 
Then run pipeline after successfully run pipeline created AKS.
 
 
(2)	Second Parts of repository to create 2 Pod , one for webserver and second for mySql server.

This script you will run from your local computer or Azur Portal CLI
Go to visual code and verify using Azure AZ login
Command:-  Kubectl create –f  “C:\Pollinate AKS”
This command find yaml and run code.
Yaml file created with 2 Pod with mysql-persistent-storage and also mount docket image to web pod.
 
 
Also create secret for mysql server password
 
Check Kubernetes pod with load balancer.
 


 







3	Website run over IP Address:- 51.138.19.206


 
