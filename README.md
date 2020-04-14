Platform-challenge
Overview
This project describes a situation that you may face in your day-to-day work at Everlywell. The goal of this project is to give you the opportunity to demonstrate your ability to solve problems, support your conclusions and communicate to stakeholders.

Requirements
Spend no more than 4 hours on the project
Fork this project and work in your repo
The tools you use to accomplish the project are your choosing
You would need access to compute and storage resources to execute this project
You would be required to speak to your process and decisions in carrying out this project

Scenario

Part 1
Imagine that you joined Everlywell at the early stages of modernizing their application. Currently, they have a Rails backend application that is hosted on a virtual machine.

Deployments are a manual which involves signing into the virtual machine, pulling down the most recent deployment branch and restarting the web server. This workflow is slow and cumbersome, and the company wants you to come up with a way to deploy the api on Kubernetes to take advantage of its many benefits.

A copy of the rails app is located in this repo in the folder rails_app.

Submission/Solution:

Attached the scripts for below tasks:
a.) Creating K8s cluster with 1 master and 2 worker nodes, with kops and running kubeclt comands for cluster and pods operations.
b.) Scripts for k8s deployment and service creation.
c.) Docker scripts for creating build image.
d.) Creating docker container runtime from images.
e.) Automating the app depolyment using Ansible scripts.
f.) Creating Jenkins pipeline for calling and invoking Ansible scripts
g.) Jenkins integrations with github which will automate the triger process, once the code commit to master branch


Part 2
The data team needs to run some analysis on a database. They ask you to provision a database daily from the most recent RDS snapshot. When the newly created database is ready for connections, run some analytics queries located on an instance in the same VPC. When the queries are done successfully executing and all the useful analysis has been extracted, delete the provisioned RDS instance for this purpose.

Given the above problem, how would you approach fulfilling the request of the data team, assuming that the tasks would take 2 hours to execute end-to-end and the task will need to be repeated daily.

Submission/Solution:

Attached are the scripts for automating the RDS snapshot creation and restoration process using Lambda functions and python scripts.
There are some automated scripts and AWS Cloud formation templates available from AWS as well which can be leveraged for this tasks. In addition, a subscription can also be created using SNS Topic ARN template creation, which will send notification emails, once the snapshot is created and restored.
Presentation and architecture diagram can be discussed as well.

Bonus
Design a deployment pipeline to deploy the rails app to your kubernetes cluster when new code is pushed to its remote branch.

Submission/Solution:
Jenkins pipeline has been created and integrated with github which will automatically trigger the build, once there are any commits made to the master branch in the code repository.
This is already covered as part 1 of the project.
