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

The first big farewell party was held on May 01, 2022 with 10 students. THANK YOU very much for the great time! 


# Available bachelor theses

* Tentative requirements analyses January-February 2022
* Tentative start February-March 2022
* Tentative finish June-December 2022


The following topics for bachelor theses are available for the summer semester 2022:


## *profileFCs*

| Title | ***profileFCs*: Characterizing and profiling *scientific* and *business* function choreographies ** |
| ----- | ----- | 
| Students | one or two | 
| Description | The aim of this bachelor thesis is to conduct a series of experiments to characterize and profile numerous function implementations of serverless applications represented as functions choreographies (FCs). FCs may be tested for various configurations (concurrency, assigned memory, latency, region, programming language, etc). The times for the functions and FCs are measured and then evaluated. The measured data is stored in a database and then statistically evaluated and visualized. The aim of this work is a better understanding of serverless computing for different FCs and FaaS systems, as well as different FCs (scientific, industry, and business). The trade-off between performance and costs will be examined more closely. The experiment will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)). 
|Tasks| 1. Develop serverless functions. <br> 2. Develop FCs in AFCL.<br> 3. Evaluate *FCs* with various workload (weak and strong scaling).|
| Theoretical skills | Cloud Computing, Serverless | 
| Practical skills | FaaS, Cloud API.|
| Related work | 1. *xAFCL* enactment engine [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137). <br> 2. Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)). |
---


## *fOps*

| Title | ***fOps*: A pipeline for one-touch development, deployment, and testing of serverless functions across multiple providers** |
| ----- | ----- | 
| Students | one or two | 
| Description |  The goal of this bachelor thesis is to develop a CI/CD pipeline for development, deployment, and functional testing of serverless functions across multiple providers. The main approach is to minimize the development effort and automatize the deployment and testing of the code for multiple FaaS providers (e.g., AWS, IBM, Google, Azure, Alibaba). The developer needs to develop the function locally only once (*function template*) and after pushing the code on git (eg. github), *fOps* pipeline will conduct a series of actions. First, *fOps* will encapsulate the code (*function implementation* - *FI*) for the selected programming language (e.g., Node.js, Go) for each supported FaaS provider. Second, *fOps* will deploy the code (FI) for each specified *function deployment* - *FD* (e.g. in MariaDB AFCL metadata database), which may include deploy the code on various cloud regions of multiple FaaS providers and determine the minimum needed memory, run the code with some predefined data inputs and test whether the code runs successfully on each FaaS provider. Finally, *fOps* stores deployment times, package size, resource link, and minimum memory in the existing AFCL metadata database for all FDs. *fOps* may consider to deploy multiple functions from a single code with multiple handlers and functions may be developed with fService and then also tests should check if the function may use all enumerated services. *fOps* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Develop a module for pipeline scripts. <br> 2. Develop wrappers for serverless function handlers for the selected programming language for various FaaS providers (e.g. AWS, IBM, Google, etc). <br> 3. Develop interfaces with AFCL metadata DB. <br> 4. Develop an automatic deployer for various FaaS providers (e.g. AWS, IBM, Google, etc).<br> 5. Evaluate *fOps* with real life applications.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Programming languages, Cloud APIs, git.|
| Related work | 1. (`Automatic function deployment`) R. Cordingly, H. Yu, V. Hoang, Z. Sadeghi, D. Foster, D. Perez, R. Hatchett, and W. Lloyd. "The Serverless Application Analytics Framework: Enabling Design Trade-off Evaluation for Serverless Software." In 2020 21st ACM/IFIP International Middleware Conference: 6th International Workshop on Serverless Computing (WoSC'20). 2020, [SAAF](https://github.com/wlloyduw/SAAF). This tools can be used for wrappers and deployment scripts for various programming languages and FaaS providers. <br> 2. (`Node.js FaaSifier`) S. Ristov, S. Pedratscher, J. Wallnöfer, and T. Fahringer, “DAF: Dependency-Aware FaaSifier for Node.js Monolithic Applications,” in IEEE Software, doi: 10.1109/MS.2020.3018334, [DAF](https://github.com/qngapparat/daf).<br> 3. (`Automatic function deployment`) [Terraform](https://www.terraform.io/).<br> 4. (`Automatic function deployment`) [Serverless](https://www.serverless.com/).<br>  5. (`Node2FaaS Framework`) [Node2FaaS *FCifier*](https://github.com/node2faas/framework).<br> 6. https://keptn.sh/.|
---

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

## *fServiceX*

| Title | ***fServiceX*: Agile development and dynamic setup of serverless applications with abstract cloud services** |
| - | - | 
| Students | one or two | 
| Description | Development of serverless functions that use multiple cloud services is a complex task as it may require huge development effort to integrate various libraries for each cloud service that the function uses. Recently, I supervised the bachelor thesis *fService: Configurable abstraction for serverless development* in which we established the main abstraction of cloud services through abstraction of AWS's and Google's storages and object recognition cloud services for java serverless functions. The library can be added as Maven dependency in Java functions. Further on, two other bachelor theses are active (*pyStorage* and *portableGo*), which extend the concept of *fService* for abstract storage in Python and Go. This bachelor thesis extends *fService* to support various programming languages (e.g., Java, node.js, Python, etc.) and various cloud services (e.g., storage, object recognition, prediction, speech2text, text2speech, etc) of multiple cloud providers (e.g., AWS, Google, etc). Heuristics may be added to determine which specific cloud service to be used (e.g., Amazon Transcribe or Google SpeechtoText) based on the storage location of the audio file. 
|Tasks| 1. Define interfaces and methods for the selected cloud storages. For instance, copy(sourceURL, destURL), voice2text(sourceAudio, destText).<br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) and their abstracted services in selected programming language(s). <br> 3. Build portable function choreography (*FC*) for a real-life application with dynamic inputs of serverless functions to specify the specific cloud service that they use (e.g. location of the input audio files).<br> 4. (if two students) Develop a model for portable cloud services used by FC functions.<br> 5. (if two students) Based on the model, develop a scheduler that updates the FC (function deployments and service deployments as data inputs).<br> 6. Evaluate the system with the developed FC and optimal selection of the proper cloud service.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | programming languages; Cloud APIs.|
| Related work| 1. B. Hackstock, "fService: Configurable abstraction for serverless development", Bachelor thesis, WS2021. |

---

# Recently started bachelor theses (SS2022)

Details for active bachelor theses can be found [here](./active/README.md).

## *profileFCSystems*

| Title | Profiling various serverless workflow management systems |
| ----- | ----- | 
| Student | Tom Giersiepen | 
| Status | Development | 
| Description | The aim of this bachelor thesis is to conduct a series of experiments to profile various serverless workflow (FC) management systems of well-known public cloud providers. FCs may be tested for various configurations (concurrency, assigned memory, latency, region, programming language, etc). The times for the functions and FCs are measured and then evaluated. The measured data is stored in a database and then statistically evaluated and visualized. The aim of this work is a better understanding of serverless computing for different FCs and FaaS systems. The trade-off between performance and costs will be examined more closely. At the end, the optimal solution will be will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)). 
---

## *InteropFCs*

| Title | **Characterizing AFCL serverless workflows with interoperable cloud services** |
| ----- | ----- | 
| Student | Florian Unterhofer | 
| Status | Development | 
| Description | Each cloud provider offers their own services for specific needs of the users. For instance, for storing objects, Amazon and Google have has AWS S3 Storage and Google Cloud Storage, respectively, while for object recognition in images, they introduced AWS Rekognition and Google Vision. In order to unlock the users in federated clouds, the novel fService approach offers developers to create serverless functions with interoperable services. With this approach, users can freely select varios services. For instance, run computing on AWS Lambda while images are stored on Google Cloud Storage and processed with AWS Rekognition. The goal of this bachelor thesis is to develop and characterize serverless applications that can easily select cloud services during runtime. The FCs will be developed using our Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)). A series of experiments will be conducted to determine pros and cons of mixing computing and cloud services among various providers (e.g., Amazon and Google). The target is to characterize how various interoperable services affect performance and cost for various problem size. For the experiments, the *xAFCL* enactment engine [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137) will be used. The final goal is to determine the fastest and cheapest setup for the evaluated FCs.|
---

## *CardioStream*

| Title | ***CardioStream*: Simulation of serverless real-time monitoring centre with streaming** |
| ----- | ----- | 
| Student | Andrei Amza | 
| Status | Requirements analysis | 
| Description | The goal of this bachelor thesis is to develop real-time monitoring centre of patients' sensor data with streaming. Simulation of real-time monitoring centre includes experiment setup, simulation, and evaluation phases. The set of actions should be performed in a form of event-based actions of the cloud provider (e.g., AWS) after streaming the patients' data. This includes serverless functions for noise intervals identification and elimination, heartbeat detection, detection of fibrillation, identification of segments and elevation, heart rate variability, statistical analysis and alerting. A smart scheduler will be developed to optimize cost-performance ratio by grouping multiple samples into a single message. The evaluation metrics will include measuring of response times for different test cases varying the workload (e.g., from 1K to 20K virtual patients ECG data simultaneously and their length). The experiment will be executed. The target is to measure speedup, cost, and throughput for various workload.|
---

## *SLO-AFCL*

| Title | ***SLO-AFCL*: FaaScinating resilience for function choreographies using service level objectives (SLOs)** |
| - | - | 
| Students | Julian Thöni and Benjamin Knjisa |
| Status | System architecture | 
| Description |  ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) may run alternative *function deployments* (*FDs*) of a serverless workflow or function choreography (*FC*) in AFCL across the top five FaaS providers. It also can log various cost, performance, and fault tolerance parameters of functions and entire FCs. However, having a proactive component that will dynamically adapt which FDs and alternatives to run will improve its resilience. An example of SLO (service level objectives) for an FC would be minimum 99% of all executions will succeed, with maximum cost of 5$ and finish within 2 seconds. Thresholds may be failure rate of each function is maximum 0.5%. This bachelor thesis will adaptively determine which FD and which alternatives to run for each FC function based on specified SLOs, which can be defined for different parameters of functions (round trip time, cost, failure rate), for the FC (makespan, cost), for specific cloud region, and for different time period (in the last minute, hour, day, etc). *SLO-AFCL* can create and select new FDs in other cloud regions (twins), in the same cloud region with more or less memory (siblings), more FDs in parallel to increase availability, etc. *SLO-AFCL* will be evaluated with a real life workflow for various FaaS providers.|
---


## *CardioAFCL*

| Title | ***CardioAFCL*: Simulation of serverless real-time monitoring centre with AFCL workflows** |
| ----- | ----- | 
| Student | Katrin Antholzer | 
| Status | Requirements analysis | 
| Description | The goal of this bachelor thesis is to develop real-time monitoring centre of patients' sensor data using batch processing approach with AFCL. Simulation of real-time monitoring centre includes experiment setup, simulation, and evaluation phases. The set of actions should be performed in a form of an AFCL serverless workflow or function choreography (*FC*) after upload of patients' data. This includes serverless functions for noise intervals identification and elimination, heartbeat detection, detection of fibrillation, identification of segments and elevation, heart rate variability, statistical analysis, alerting, and reporting. A generator of a virtual patient ECG will be developed to simulate generated files. The evaluation metrics will include measuring of response times for different test cases varying the workload (e.g., from 1K to 20K virtual patients ECG data simultaneously and their length). The experiment will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)). The target is to measure speedup and throughput versus the number of cloud regions (<3 sec).|
---

## *xAFCLSim2*

| Title | ***xAFCLSim2*: Simulation of serverless workflows in AFCL with dependent cloud services** |
| ----- | ----- | 
| Students | Marcel Huber and Matthias Thalmann | 
| Status | Development | 
| Description |  Running highly scalable FCs may be a long running and costly operation. Recently, I supervised the bachelor thesis "*xAFCLSim* simulation framework" in which the initial version of the xAFCL simulator was integrated in xAFCL enactment engine, which assumes compute intensive serverless functions. The goal of this bachelor thesis is to develop *xAFCLSim2* simulation framework, which will support simulation of serverless functions that use cloud services (e.g., cloud storage), which can be dynamically selected as input to the functions. A dynamism will be added based on some known distributions. FCs are built with the existing [Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)) and run with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)), in which *xAFCLSim2* will be integrated into. *xAFCLSim2* will be evaluated with real life functions for various FaaS providers and abstracted cloud services. The main target will be to simulate the round trip time of, for instance, a serverless function that runs in AWS Frankfurt and downloads the input file from AWS S3 Tokyo and stores the output file in Google Cloud Storage in Belgium if we have executed the same function implementation on any AWS region (not on another provider) with any storage location for input and output files (even on Google storage).|
---


## *pyfOps*

| Title | ***pyfOps*: A pipeline for one-touch development, deployment, and testing of Python serverless functions across multiple providers**|
| ----- | ----- | 
| Student | Serafin Plattner | 
| Status | Development | 
| Description |  The goal of this bachelor thesis is to develop a CI/CD pipeline for development, deployment, and functional testing of Python serverless functions across multiple providers. The main approach is to minimize the development effort and automatize the deployment and testing of the code for multiple FaaS providers (e.g., AWS, IBM, Google, Azure, Alibaba). The developer needs to develop the function in Python locally only once (*function template*) and after pushing the code on git (eg. github), *pyfOps* pipeline will conduct a series of actions. First, *pyfOps* will encapsulate the code (*function implementation* - *FI*) for each supported FaaS provider. Second, *pyfOps* will deploy the python code (FI) for each specified *function deployment* - *FD* (e.g. in MariaDB AFCL metadata database), which may include deploy the Python code on various cloud regions of multiple FaaS providers and determine the minimum needed memory, run the code with some predefined data inputs and test whether the code runs successfully on each FaaS provider. Finally, *pyfOps* stores deployment times, package size, resource link, and minimum memory in the existing AFCL metadata database for all FIs and FDs. *pyfOps* may consider to deploy multiple functions from a single code with multiple handlers and functions may be developed with fService and then also tests should check if the function may use all enumerated services. *pyfOps* will be evaluated with a real life workflow for various FaaS providers.|

---

## *jfOps*

| Title | ***jfOps*: A pipeline for one-touch development, deployment, and testing of Java serverless functions across multiple providers** (Tentative) |
| ----- | ----- | 
| Students | Thomas Pregenzer and Tobias Hosp | 
| Status | System architecture | 
| Description |  The goal of this bachelor thesis is to develop a CI/CD pipeline for development, deployment, and functional testing of Java serverless functions across multiple providers. The main approach is to minimize the development effort and automatize the deployment and testing of the code for multiple FaaS providers (e.g., AWS, IBM, Google, Azure, Alibaba). The developer needs to develop the function in Java locally only once (*function template*) and after pushing the code on git (eg. github), *jfOps* pipeline will conduct a series of actions. First, *jfOps* will encapsulate the Java code (*function implementation* - *FI*) for each supported FaaS provider. Second, *jfOps* will deploy the code (FI) for each specified *function deployment* - *FD* (e.g. in MariaDB AFCL metadata database), which may include deploy the code on various cloud regions of multiple FaaS providers and determine the minimum needed memory, run the code with some predefined data inputs and test whether the code runs successfully on each FaaS provider. Finally, *jfOps* stores deployment times, package size, resource link, and minimum memory in the existing AFCL metadata database for all FIs and FDs. *jfOps* may consider to deploy multiple functions from a single code with multiple handlers and functions may be developed with fService and then also tests should check if the function may use all enumerated services. *jfOps* will be evaluated with a real life workflow for various FaaS providers.|
---


## *testOps*

| Title | ***testOps*: A pipeline for one-touch non-functional testing of serverless functions across multiple providers** (Tentative) |
| ----- | ----- | 
| Student | Thomas Zangerl | 
| Status | Requirements analysis | 
| Description |  The goal of this bachelor thesis is to develop an automation pipeline for non-functinoal testing of serverless functions and infrastructure across multiple providers. The main objective is to minimize the effort and automatize the language-agnostic testing of arbitrary function implementations (*FIs*), or the deployment packages for multiple FaaS providers (e.g., AWS, IBM, Google, Azure, and Alibaba). The Ops engineer needs to deploy the deployment package (jar or zip) for each specified *function deployment* - *FD* in the test plan, which may include deploy the package on various cloud regions and run the code with some predefined various performance parameters (RTT, ET, concurrency limitations, various cloud services abstracted with fService) and store the measured parameters in the existing AFCL metadata database for all FDs. *testOps* will evaluate serverless infrastructures with "no-op" functions and real life functions for various FaaS providers and abstracted cloud services with fService.|
---

## *portableGo*

| Title | ***portableGo*: Portable development and deployment of Go functions in serverless workflows** |
| ----- | ----- | 
| Student | Simon Brandacher | 
| Status | Evaluation | 
| Description |  *portableGo* will be implemented to support serverless functions developed in Golang and storage services from multiple cloud providers (e.g., AWS, Google, etc). Furthermore, *portableGo* will offer automatic deployment on multiple clouds from a single developed function locally. Finally, *portableGo* will be integrated with AFCL workflows to deploy each function of a workflow to the specified location (FaaS provider, cloud region, and assigned memory.)|
---

## *xAFCL* Data-Flow

| Title | ***xAFCL* data-flow** |
| ----- | ----- | 
| Student | Andreas Reheis | 
| Status | Development | 
| Description | The goal of this thesis is to facilitate the development of FCs with data-flow between abstract function types. After development, the system will convert the abstract into concrete data-flow during runtime.|
---

<!-- Details for active bachelor theses can be found [here](./active/README.md). -->


# Closed bachelor theses

1. "*pyStorage*: Agile development and optimized execution of data-intensive serverless workflows", Isabella Schmut and Peter Koll. SS2022. [details](./closed/pyStorage.md).
1. "*pyFCfier*: Portable Python FCifier", Mark Nardi. SS2022. [details](./closed/pyFCfier.md).
1. "*jContainer*: Portable execution of FCs across multiple container systems", David Baumgartner and Albert Neuner. WS2021. [details](./closed/jContainer.md).
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

My topics for master theses may be found [here](https://github.com/sashkoristov/master-theses), which could also be adapted as bachelor theses.