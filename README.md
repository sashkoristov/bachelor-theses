# Bachelor theses (Supervisor: Sashko Ristov)

A repository for available, active and closed topics for bachelor theses in the context of the class “Seminar mit Bachelorarbeit”. Supervisor - Dr. Sashko Ristov.

<!--
As a result of several bachelor and master theses that I supervised, we have developed a prototype of the *xAFCL* enactment engine [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137), which is able to run serverless workflows or function choreographies (*FCs*) across many widely-known cloud providers. *xAFCL EE* integrates the component [FTjFaaS](https://github.com/sashkoristov/FTjFaaS) for optional fault tolerant execution of FC functions (currently supported AWS Lambda and IBM Cloud Functions) and [jFaaS](https://github.com/sashkoristov/jFaaS/) for portable execution across many FaaS systems (AWS Lambda, IBM Cloud Functions, Google Cloud Functions, Alibaba Function Compute, Microsoft Azure Cloud Functions, etc).

*xAFCL EE* is the core part of the [AFCL Environment](https://github.com/sashkoristov/AFCLEnvironment), a platform to develop, deploy, and fault tolerant execution of FCs developed in our Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)).
-->

The following paragraphs present the available bachelor theses for the following upcoming summer semester 2023. 

You can find a latex template for the bachelor thesis which includes some hints [here](https://github.com/sashkoristov/bachelor-theses/tree/main/template).

Topics are inintially intended for a single student, but each topic can be adapted for a group of two students.

---

# New available topics for SS2023



## Topics

The following topics for bachelor theses are available for the summer semester 2023:


1. *StreamAFCL* : A novel serverless workflow management system for streaming AFCL workflows in federated FaaS [details](./new/StreamAFCL.md).
1. *TwinLess* : Building a digital twin with serverless workflows in federated FaaS.
1. *fServiceX* : Code once serverless functions and dynamically select BaaS services in federated FaaS [details](./new/fServiceX.md).
1. *fOps*: Automation in packaging, deployment, and testing of serverless functions in federated FaaS [details](./new/fOps.md).
1. *ProfileBaaS*: Characterizing and profiling Backend-as-a-Service in Federated FaaS [details](./new/profileBaaS.md).


## Timeline

* Tentative application by students: January - February 2023
* Tentative start with the thesis:  March 2023 - April 2023
* Tentative finish June - December 2023

## Tentative agenda

We will define several milestones for the project and ideally bi-weekly meetings for project status. 

 

## General milestones for a successful bachelor thesis

- Requirements analysis
- System architecture
- Initial presentation
- Development
- Evaluation
- Finalizing the bachelor thesis
- Final presentation
- `Farewell party` :blush:



<!--
## *AFCLOps*

| Title | ***AFCLOps*: A pipeline for deployment of AFCL serverless workflows across multiple providers** |
| ----- | ----- | 
| Students | one |
| Description | The goal of this bachelor thesis is to develop a pipeline for deployment of serverless functions (*function deployments* - *FDs*) of a given AFCL serverless workflow or *function choreography* (*FC*) defined in AFCL. The main approach is to automatize deployment of all FDs of an FC that are not deployed from existing function implementations (*FIs*) when the AFCL file is pushed on git or before running it. The FC developer pushes an AFCL file to github and *AFCLOps* parses it to determine each base function and gets specification from MariaDB database. Based on that, *AFCLOps* deploys all specified functions. AFCLOps checks in the AFCL metadata DB the locations of deployment packages (e.g., codes on gitFaaSDeploy repository). To speed up the process, *AFCLOps* will create an FC that will run deployers (serverless functions) in parallel. In case of a failed deployment, another FD of the same implementation or an FD of on another FI of the same *function type* (*FT*) based on some objectives that will be defined during the thesis. At the same time, the AFCL file will be updated. *AFCLOps* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Develop a module for pipeline scripts. <br> 2. Develop a module to adapt the FC for parallel execution of deployers. <br> 3. Develop interfaces with AFCL metadata DB. <br> 4. Develop an automatic deployer for various FaaS providers (e.g. AWS, IBM, Google, etc).<br> 5. Evaluate *fOps* with real life FCs applications.|
| Theoretical skills | Cloud Computing, Serverless, AFCL, fault tolerance. | 
| Practical skills | Cloud APIs, git.|
| Related work | 1. SAAF https://github.com/wlloyduw/SAAF. This tools can be used for wrappers and deployment scripts for various programming languages and FaaS providers.<br> 2. ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) S. Ristov, S. Pedratscher, T. Fahringer, “xAFCL: Run scalable function choreographies across multiple FaaS systems,” in *IEEE Transactions on Services Computing*, pp. 1–1, 2021. ([doi](https://doi.org/10.1109/TSC.2021.3128137))<br> 3. S. Ristov, S. Pedratscher, T. Fahringer, "AFCL: An Abstract Function Choreography Language for serverless workflow specification", in *Elsevier Future Generation Computer Systems*, vol. 114, pp. 368-382, 2021. ([doi](https://doi.org/10.1016/j.future.2020.08.012))|
---
-->




<!--
# Recently started bachelor theses (SS2023)
-->



# Active bachelor theses

Details for active bachelor theses can be found [here](./active/README.md).

1. "*GoSpeechLess*: An interoperable library for serverless functions in Go to convert speech and text", David Meyer. [details](./active/GoSpeechLess.md).
1. "*profileCold*: Characterizing and modeling cold start overhead in federated FaaS", Maximilian Gallinat. [details](./active/profileCold.md).
1. "*pyRecognition*: An interoperable programming and execution model for object recognition in Federated FaaS, Lea Plangger. [details](./active/pyRecognition.md).
1. "*MatchFaaS*: Matching-based Scheduling of Serverless Workflows in Federated FaaS", Amza Andrei. [details](./active/MatchFaaS.md).
1. "*profileFCs*: Characterizing *scientific* function choreographies with xAFCL in federated FaaS", Fabian Dria. [details](./profileFCs.md).
1. "*SLO-AFCL*: FaaScinating resilience for function choreographies using service level objectives (SLOs)", Julian Thöni and Benjamin Knjisa. [details](./SLO-AFCL.md).




# Closed bachelor theses

Details for closed bachelor theses can be found [here](./closed/README.md).



# Contact

If you need any additional information, please do not hesitate to contact me on e-mail.

My topics for master theses may be found [here](https://github.com/sashkoristov/master-theses), which could also be adapted as bachelor theses.

