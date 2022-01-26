# Bachelor theses (Supervisor: Sashko Ristov)
A repository for available, active and closed topics for bachelor theses in the context of the class “Seminar mit Bachelorarbeit”. Supervisor - Sashko Ristov.

As a result of several bachelor and master theses that I supervised, we have developed a prototype of the *xAFCL* enactment engine [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137), which is able to run serverless workflows or function choreographies (*FCs*) across many widely-known cloud providers. *xAFCL EE* integrates the component [FTjFaaS](https://github.com/sashkoristov/FTjFaaS) for optional fault tolerant execution of FC functions (currently supported AWS Lambda and IBM Cloud Functions) and [jFaaS](https://github.com/sashkoristov/jFaaS/) for portable execution across many FaaS systems (AWS Lambda, IBM Cloud Functions, Google Cloud Functions, Alibaba Function Compute, Microsoft Azure Cloud Functions, etc).

*xAFCL EE* is the core part of the [AFCL Environment](https://github.com/sashkoristov/AFCLEnvironment), a platform to develop, deploy, and fault tolerant execution of FCs developed in our Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)).

The following paragraphs present the available and recently started bachelor theses. It also sumarizes the active and closed bachelor theses. 

You can find a latex template for the bachelor thesis which includes some hints [here](https://github.com/sashkoristov/bachelor-theses/tree/main/template).

Topics are inintially intended for a single student, but each topic can be adapted for a group of two students.

## Milestones for a successful bachelor thesis

- Requirements analysis
- System architecture
- Initial presentation
- Development
- Evaluation
- Finalizing the bachelor thesis
- Final presentation
- `Farewell party` :blush:

# Available bachelor theses

* Tentative requirements analyses January-February 2022
* Tentative start February-March 2022
* Tentative finish June-December 2022


The following topics for bachelor theses are available for the summer semester 2022:


## *fOps*

| Title | ***fOps*: A pipeline for one-touch development, deployment, and testing of serverless functions across multiple providers** |
| ----- | ----- | 
| Students | one or two | 
| Description |  The goal of this bachelor thesis is to develop a CI/CD pipeline for development, deployment, and testing of serverless functions across multiple providers. The main approach is to minimize the development effort and automatize the deployment and testing of the code for multiple FaaS providers (e.g., AWS, IBM, Google, Azure, Alibaba). The developer needs to develop the function locally only once (*function template*) and after pushing the code on git (eg. github), *fOps* pipeline will conduct a series actions. First, *fOps* will encapsulate the code (*function implementation* - *FI*) for the selected programming language (e.g., Java, Python, Node.js, Go) for each supported FaaS provider. Second, *fOps* will deploy the code (FI) for each specified *function deployment* - *FD* (e.g. in MariaDB AFCL metadata database), which may include deploy the code on various cloud regions of multiple FaaS providers and determine the minimum needed memory, run the code with some predefined data inputs and test whether the code runs successfully on each FaaS provider. Finally, *fOps* stores deployment times, package size, resource link, round trip time, and minimum memory in the existing AFCL metadata database for all FDs. *fOps* may consider to deploy multiple functions from a single code with multiple handlers. *fOps* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Develop a module for pipeline scripts. <br> 2. Develop wrappers for serverless function handlers for the selected programming languages for various FaaS providers (e.g. AWS, IBM, Google, etc). <br> 3. Develop interfaces with AFCL metadata DB. <br> 4. Develop an automatic deployer for various FaaS providers (e.g. AWS, IBM, Google, etc).<br> 5. Evaluate *fOps* with real life applications.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Programming languages, Cloud APIs, git.|
| Related work | 1. 3. (`Automatic function deployment`) R. Cordingly, H. Yu, V. Hoang, Z. Sadeghi, D. Foster, D. Perez, R. Hatchett, and W. Lloyd. "The Serverless Application Analytics Framework: Enabling Design Trade-off Evaluation for Serverless Software." In 2020 21st ACM/IFIP International Middleware Conference: 6th International Workshop on Serverless Computing (WoSC'20). 2020, [SAAF](https://github.com/wlloyduw/SAAF). This tools can be used for wrappers and deployment scripts for various programming languages and FaaS providers. <br> 2. (`Node.js FaaSifier`) S. Ristov, S. Pedratscher, J. Wallnöfer, and T. Fahringer, “DAF: Dependency-Aware FaaSifier for Node.js Monolithic Applications,” in IEEE Software, doi: 10.1109/MS.2020.3018334, [DAF](https://github.com/qngapparat/daf).<br> 3. (`Automatic function deployment`) [Terraform](https://www.terraform.io/).<br> 4. (`Automatic function deployment`) [Serverless](https://www.serverless.com/).<br>  5. (`Node2FaaS Framework`) [Node2FaaS *FCifier*](https://github.com/node2faas/framework).|
---


## *AFCLOps*

| Title | ***AFCLOps*: A pipeline for deployment of AFCL serverless workflows across multiple providers** |
| ----- | ----- | 
| Students | one |
| Description | The goal of this bachelor thesis is to develop a pipeline for deployment of serverless functions (*function deployments* - *FDs*) of a given AFCL serverless workflow or *function choreography* (*FC*) defined in AFCL. The main approach is to automatize deployment of all FDs of an FC that are not deployed from existing function implementations (*FIs*) when the AFCL file is pushed on git or before running it. The FC developer pushes an AFCL file to github and *AFCLOps* parses it to determine each base function and gets specification from MariaDB database. Based on that, *AFCLOps* deploys all specified functions. AFCLOps checks in the AFCL metadata DB the locations of deployment packages (e.g., codes on gitFaaSDeploy repository). To speed up the process, *AFCLOps* will create an FC that will run deployers (serverless functions) in parallel. In case of a failed deployment, another FD of the same implementation or an FD of on another FI of the same *function type* (*FT*) based on some objectives that will be defined during the thesis. At the same time, the AFCL file will be updated. *AFCLOps* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Develop a module for pipeline scripts. <br> 2. Develop a module to adapt the FC for parallel execution of deployers. <br> 3. Develop interfaces with AFCL metadata DB. <br> 4. Develop an automatic deployer for various FaaS providers (e.g. AWS, IBM, Google, etc).<br> 5. Evaluate *fOps* with real life FCs applications.|
| Theoretical skills | Cloud Computing, Serverless, AFCL, fault tolerance. | 
| Practical skills | Cloud APIs, git.|
| Related work | 1. SAAF https://github.com/wlloyduw/SAAF. This tools can be used for wrappers and deployment scripts for various programming languages and FaaS providers.<br> 2. ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) S. Ristov, S. Pedratscher, T. Fahringer, “xAFCL: Run scalable function choreographies across multiple FaaS systems,” in \textit{IEEE Transactions on Services Computing}, pp. 1–1, 2021. ([doi](https://doi.org/10.1109/TSC.2021.3128137))<br> 3. S. Ristov, S. Pedratscher, T. Fahringer, "AFCL: An Abstract Function Choreography Language for serverless workflow specification", in \textit{Elsevier Future Generation Computer Systems}, vol. 114, pp. 368-382, 2021. ([doi](https://doi.org/10.1016/j.future.2020.08.012))|
---

## *fServiceX*

| Title | ***fServiceX*: Agile development of serverless applications with abstract cloud services** |
| - | - | 
| Students | one or two | 
| Description | Development of serverless functions that use multiple cloud services is a complex task as it may require huge development effort to integrate various libraries for each cloud service that the function uses. Recently, I supervised the bachelor thesis *fService: Configurable abstraction for serverless development* in which we established the main abstraction of cloud services through abstraction of AWS's and Google's storages and object recognition cloud services for java serverless functions. The library can be added as Maven dependency in Java functions. Further on, two other bachelor theses are active (*pyStorage* and *portableGo*), which extend the concept of *fService* for abstract storage in Python and Go. This bachelor thesis extends *fService* to support various programming languages (e.g., Java, node.js, Python, etc.) and various cloud services (e.g., storage, object recognition, prediction, speech2text, text2speech, etc) of multiple cloud providers (e.g., AWS, Google, etc). Heuristics may be added to determine which specific cloud service to be used (e.g., Amazon Transcribe or Google SpeechtoText) based on the storage location of the audio file. 
|Tasks| 1. Define interfaces and methods for the selected cloud storages. For instance, copy(sourceURL, destURL), voice2text(sourceAudio, destText).<br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) and their abstracted services in selected programming language(s). <br> 3. Build portable function choreography (*FC*) for a real-life application with dynamic inputs of serverless functions to specify the specific cloud service that they use (e.g. location of the input audio files).<br> 4. (if two students) Develop a model for portable cloud services used by FC functions.<br> 5. (if two students) Based on the model, develop a scheduler that updates the FC (function deployments and service deployments as data inputs).<br> 6. Evaluate the system with the developed FC and optimal selection of the proper cloud service.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | programming languages; Cloud APIs.|
---

## *SLO-AFCL*

| Title | ***SLO-AFCL*: FaaScinating resilience for function choreographies using service level objectives (SLOs)** |
| - | - | 
| Students | one or two |
| Description |  ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) may run alternative *function deployments* (*FDs*) of a serverless workflow or function choreography (*FC*) in AFCL across the top five FaaS providers. It also can log various cost, performance, and fault tolerance parameters of functions and entire FCs. However, having a proactive component that will dynamically adapt which FDs and alternatives to run will improve its resilience. An example of SLO (service level objectives) for an FC would be minimum 99% of all executions will succeed, with maximum cost of 5$ and finish within 2 seconds. Thresholds may be failure rate of each function is maximum 0.5%. This bachelor thesis will adaptively determine which FD and which alternatives to run for each FC function based on specified SLOs, which can be defined for different parameters of functions (round trip time, cost, failure rate), for the FC (makespan, cost), for specific cloud region, and for different time period (in the last minute, hour, day, etc). *SLO-AFCL* can create and select new FDs in other cloud regions (twins), in the same cloud region with more or less memory (siblings), more FDs in parallel to increase availability, etc. *SLO-AFCL* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Research parameters that can be used to define SLOs ranges and thresholds including parameters of functions, time periods, FC, cloud providers and their regions, etc.<br> 2. Develop interfaces with AFCL metadata DB.<br> 3. Develop / adapt monitoring for SLOs.<br> 4. Develop an AFCL adaptor that will adapt resource FDs and alternatives.<br> 5. Visualize SLO parameters.<br> 6. Evaluate *SL-AFCL* with the real-life FC and specific scenarios that try to breach SLOs.|
| Theoretical skills | Cloud Computing, Serverless, AFCL, fault tolerance. | 
| Practical skills | Algorithms, Cloud APIs.|
| Related work | 1. [Google SRE](https://sre.google/)

# Recently started bachelor theses (SS2022)

## *portableGo*

| Title | ***portableGo*: Portable development and deployment of Go functions in serverless workflows** |
| ----- | ----- | 
| Student | Simon Brandacher | 
| Status | Requirements analysis | 
| Description |  *portableGo* will be implemented to support serverless functions developed in Golang and storage services from multiple cloud providers (e.g., AWS, Google, etc). Furthermore, *portableGo* will offer automatic deployment on multiple clouds from a single developed function locally. Finally, *portableGo* will be integrated with AFCL workflows to deploy each function of a workflow to the specified location (FaaS provider, cloud region, and assigned memory.)
|Tasks| 1. Define interfaces and methods for various cloud storages. For instance, copyFile(sourceURL, destinationURL). <br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) in Golang. <br> 3. Build portable FCs for a real-life application with dynamic inputs of functions to specify the specific storages that they use.<br> 4. Develop an automatic deployer.<br> 5. Integrate with AFCL.<br> 6. Evaluate the system with real life applications.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Golang, Cloud APIs.|
---


# Active bachelor theses

## *pyStorage*

| Title | ***pyStorage*: Agile development and optimized execution of data-intensive serverless workflows** |
| ----- | ----- | 
| Students | Isabella Schmut and Peter Koll | 
| Status | Evaluation | 
| Description |  Development of serverless functions that use multiple cloud services is a complex task as it may require a huge development effort to integrate various libraries for each cloud service that the function uses. This thesis explores how to model cloud service types that a function uses in order to abstract them and offer a single interface for specific service type. *pyStorage* will be implemented to support serverless functions developed in Python programming languages and cloud storages of multiple cloud providers (e.g., AWS, Google, etc). 
|Tasks| 1. Define interfaces and methods for various cloud storages. For instance, uploadFile(bucket), downloadFile(bucket). <br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) in Python. <br> 3. Build portable FCs for a real-life application with dynamic inputs of functions to specify the specific storages that they use.<br> 4. Develop a model for portable cloud storages used by FC functions.<br> 5. Based on the model, develop a scheduler that updates the FC (function deployments and service deployments as data inputs).<br> 6. Evaluate the system with real life applications and optimal selection of the proper cloud storage.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Python, Cloud APIs.||
---

## *jContainer* 


| Title | ***jContainer*: Portable execution of FCs across multiple container systems** |
| ----- | ----- | 
| Students | David Baumgartner and Albert Neuner | 
| Status | Evaluation | 
| Description | All widely-known FaaS systems set up many design limitations (e.g., code size or memory assignment) and runtime limitations (e.g., size of input / output data, function duration, or hard disk size). The goal of this thesis is to develop a portable `jContainer` tool, which allows portable execution of FCs in multiple container systems, e.g., AWS Fargate or ECS.
|Tasks| 1. Develop a `jContainer` for multiple container systems.<br> 2. Integrate `jContainer` in *xAFCL EE*.<br> 3. Automatic container development and deployment of containers for multiple providers.<br> 4. Compose / adapt a real-life application that uses multiple cloud services.<br> 5. Evaluate `jContainer` with the real-life serverless applications across multiple container systems.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Virtualization | 
| Practical skills | Java (or Python, Node.js), Cloud APIs, Container Systems.||
---

## *xAFCL* Data-Flow

| Title | ***xAFCL* data-flow** |
| ----- | ----- | 
| Student | Andreas Reheis | 
| Status | Development | 
| Description | The goal of this thesis is to facilitate the development of FCs with data-flow between abstract function types. After development, the system will convert the abstract into concrete data-flow during runtime.|
|Tasks| 1. Graphical development of FC data-flow considering data ports interoperbility and integration with AFCL meta-data database.<br> 2. Convert abstract to concrete data-flow.<br> 3. Data-flow managament (e.g., merge data inputs/outputs, passing data, sub-objects, super-objects, DAG-based data-flow, data-flow through compound functions, ...).<br> 4. Automatic generation of AFCL/CFCL code.<br> 5. Evaluate the converted data-flow with a representative FC.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless, AFCL | 
|Practical skills | Java ||
---


## *pyFCfier*

| Title | ***pyFCfier*: Portable Python FCifier** |
| ----- | ----- | 
| Student | Mark Nardi | 
| Status | Evalluation | 
| Description |  The goal of this thesis is to develop a portable Python FCfier (*pyFCfier*), which allows the FC developer to select the target FaaS system per serverless function, faasifies parts of the monolith as serverless fynctions across multiple FaaS systems, updates the offloaded code with the corresponding API calls converts Python monoliths as FCs and evaluate their scalability.|
|Tasks| 1. Develop a Python FCifier *pyFCfier* for multiple FaaS systems.<br> 2. Compose / adapt a monolith that uses multiple cloud services.<br> 3. Code annotation (per line) in Python to be FaaSified.<br> 4. Automatic package development and serverless function deployment of the faasified code.<br> 5. Evaluate the *pyFCfier* with real-life serverless applications.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
|Practical skills | Python.||


<!-- Details for active bachelor theses can be found [here](./active/README.md). -->


# Closed bachelor theses

1. "*jFCfier*: Portable Java *FCfier*", David Freina and Jonas Wagner. WS2021. [details](./closed/jFCfier.md).
1. "*fService*: Configurable abstraction for serverless development", Benjamin Hackstock. WS2021. [details](./closed/fService.md).
1. "*xAFCLTrace* scheduling and tracing framework", Philipp Gritsch. WS2021. [details](./closed/xAFCLTrace.md).
1. "*aSync xAFCL EE*: Asynchronous enactment of FCs across multiple FaaS systems", Stefan Kotrba. WS2021. [details](./closed/asyncxAFCL.md).
1. "*xAFCLSim* simulation framework", Mika Hautz. WS2021. [details](./closed/xAFCLSim.md).
1. "A learning-based simulation framework for volatile cloud resources", Johannes Spies, Simon Triendl. SS2021. [details](./closed/volatilesimx.md).
1. "G2GA: Portable execution of workflows in Google Cloud Functions across multiple FaaS platforms", Anna Kapeller, Felix Petschko. SS2021.
1. "Decoupled Automatic Deployment of AFCL Workflows", Caroline Haller, Christoph Abenthung. SS2021.
1. "Establishing Virtual Networks in Amazon Web Services", Hüseyin Gündogan, WS2020.
1. "Function Choreography Scheduling Framework for Multiple FaaS Systems", Tobias Pockstaller, WS2020.
1. "Running workflow applications across multiple cloud providers", Marina Aichinger, SS2020.
1. "Advisor for renting virtual machines from various public cloud service providers", Thomas Wurzer, SS2020.
1. "Monitoring system for virtualized resources in a cloud data center", David Bucher, Peter Scheier, SS2020.
1. "Middleware services to support workflow execution in a Multi-FaaS environment", Jakob Wallnöfer, SS2020, `Among top five theses for 2020` at the institute.
1. High-level Modeling and Low-level Adaptation of Serverless Function Choreographies, Benjamin Walch, SS2020. [FCEditor](http://fceditor.dps.uibk.ac.at:8180/)
1. "Fault-tolerant execution of serverless functions across multiple FaaS systems", Matteo Bernard, Battaglin, SS2020. The initial version of [FTjFaaS] is integrated in [xAFCL](https://github.com/sashkoristov/enactmentengine/).
1. "Multi-layer enactment engine for workflow applications", Florian Maier, SS2020.
1. "Enactment engine for composed serverless functions in Fission FaaS framework", Dominik Kuen, SS2020.
1. "IoT Data analytics using Serverless Computing", Markus Reiter, Michael Kaltschmid, SS2020.
1. "Fault-tolerant enactment engine for workflow applications on Amazon EC2 Spot Instances", David Milic, Fabio Schett WS2019.
1. "Scalable Data Analytics in Edge Cloud Continuum", Hanna Köb, WS2019.
1. "Multi-provider enactment engine (EE) for serverless workflow applications", Jakob Nöckl, Markus Moosbrugger, SS2019. `Among top three theses for 2019` at the institute. Initial version of [xAFCL](https://github.com/sashkoristov/enactmentengine/).

Details for closed bachelor theses can be found [here](./closed/README.md).

----

# Contact

If you need any additional information, please do not hesitate to contact me on e-mail.

My topics for master theses may be found [here](https://github.com/sashkoristov/master-theses).