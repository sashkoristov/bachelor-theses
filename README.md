# Bachelor theses (Supervisor: Sashko Ristov)
A repository for available, active and closed topics for bachelor theses in the context of the class “Seminar mit Bachelorarbeit”. Supervisor - Sashko Ristov.

As a result of several bachelor and master theses that I supervised, we have developed a prototype of the *xAFCL* enactment engine, which is able to run serverless workflows or function choreographies (*FCs*) across many widely-known cloud providers. *xAFCL EE* integrates the component [FTjFaaS](https://github.com/sashkoristov/FTjFaaS) for optional fault tolerant execution of FC functions (currently supported AWS Lambda and IBM Cloud Functions) and [jFaaS](https://github.com/sashkoristov/jFaaS/) for portable execution across many FaaS systems (AWS Lambda, IBM Cloud Functions, Google Cloud Functions, Alibaba Function Compute, Microsoft Azure Cloud Functions, etc).

*xAFCL EE* is the core part of the [AFCL Environment](https://github.com/sashkoristov/AFCLEnvironment), a platform to develop, deploy, and fault tolerant execution of FCs developed in our Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)).

The following paragraphs present the available and recently started bachelor theses. It also sumarizes the active and closed bachelor theses. 

You can find a latex template for the bachelor thesis which includes some hints [here](https://github.com/sashkoristov/bachelor-theses/tree/main/template).

Milestones for a successful bachelor thesis:
- Requirements analysis
- System architecture
- Initial presentation
- Development
- Evaluation
- Finalizing the bachelor thesis
- Final presentation
- `Farewell party` :blush:

<!--
# Available bachelor theses / ideas

* Tentative requirements analyses January-February 2021
* Tentative start February-March 2021
* Tentative finish June-December 2021

The following topics for bachelor theses are available for the summer semester 2021.

## 2. AFCL vs-code IntelliSense

Initial idea: build the FC using VS-code, but with intelligent proposal to fill the code (IntelliSense). For more information, please contact me on sashko@dps.uibk.ac.at.
-->
----

# Recently started bachelor theses (SS2021)

## *pyStorage*

| Title | ***pyStorage*: Agile development and optimized execution of data-intensive serverless workflows** |
| ----- | ----- | 
| Students | Isabella Schmut and Peter Koll | 
| Status | Development | 
| Description |  Development of serverless functions that use multiple cloud services is a complex task as it may require a huge development effort to integrate various libraries for each cloud service that the function uses. This thesis explores how to model cloud service types that a function uses in order to abstract them and offer a single interface for specific service type. *pyStorage* will be implemented to support serverless functions developed in Python programming languages and cloud storages of multiple cloud providers (e.g., AWS, Google, etc). 
|Tasks| 1. Define interfaces and methods for various cloud storages. For instance, uploadFile(bucket), downloadFile(bucket). <br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) in Python. <br> 3. Build portable FCs for a real-life application with dynamic inputs of functions to specify the specific storages that they use.<br> 4. Develop a model for portable cloud storages used by FC functions.<br> 5. Based on the model, develop a scheduler that updates the FC (function deployments and service deployments as data inputs).<br> 6. Evaluate the system with real life applications and optimal selection of the proper cloud storage.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Python, Cloud APIs.||
---


## *fService*

| Title | ***fService*: Configurable abstraction for serverless development** |
| ----- | ----- | 
| Student | Benjamin Hackstock | 
| Status | Finalizing the bachelor thesis | 
| Description |  Development of serverless functions that use multiple cloud services is a complex task as it may require a huge development effort to integrate various libraries for each cloud service that the function uses. This thesis explores how to model cloud service types that a function uses in order to abstract them and offer a single interface with various methods for specific tasks. *fService* will be implemented to support various programming languages (e.g., Java, node.js, Python, etc.) and several cloud services (e.g., storage, object recognition, prediction, etc) of multiple cloud providers (e.g., AWS, Google, etc).
|Tasks| 1. Define interfaces and methods for various cloud services (e.g., storage, object recognition, prediction, etc). For instance, uploadFile(bucket), downloadFile(bucket). <br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc).<br> 3. Develop implementations of interfaces for various programming languages (e.g., Java, node.js, Python, etc).<br> 4. Build a portable FC for a real-life application with dynamic inputs of functions to specify the specific services that they use.<br> 5. Evaluate the system with real life applications and optimal selection of the proper cloud service.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Java, Python, or Node.js; Cloud APIs.||
---


## *jContainer* 

<!-- Based on your preferences regarding the programming language, you can select to work on *jContainer*, *PyContainer*, or *jsContainer*. It is also possible to work in a team of two students using two different proframming languages.
-->

| Title | ***jContainer*: Portable execution of FCs across multiple container systems** |
| ----- | ----- | 
| Students | David Baumgartner and Albert Neuner | 
| Status | Development | 
| Description | All widely-known FaaS systems set up many design limitations (e.g., code size or memory assignment) and runtime limitations (e.g., size of input / output data, function duration, or hard disk size). The goal of this thesis is to develop a portable `jContainer` tool, which allows portable execution of FCs in multiple container systems, e.g., AWS Fargate or ECS.
|Tasks| 1. Develop a `jContainer` for multiple container systems.<br> 2. Integrate `jContainer` in *xAFCL EE*.<br> 3. Automatic container development and deployment of containers for multiple providers.<br> 4. Compose / adapt a real-life application that uses multiple cloud services.<br> 5. Evaluate `jContainer` with the real-life serverless applications across multiple container systems.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Virtualization | 
| Practical skills | Java (or Python, Node.js), Cloud APIs, Container Systems.||
---

## *aSync xAFCL EE*

| Title | ***aSync xAFCL EE*: Asynchronous enactment of FCs across multiple FaaS systems** |
| ----- | ----- | 
| Student | Stefan Kotrba | 
| Status | Finalizing the bachelor thesis | 
| Description | All widely-known FaaS systems allow asynchronous invocation of serverless functions. The goal of this bachelor thesis is to develop the *aSync xAFCL EE* which will be able to enact *FCs* asynchronously across multiple FaaS systems.
|Tasks| 1. Review the existing workflow management systems (WMSs) that support asynchronous invocation.<br> 2. Analyze the behavior of FaaS systems over asynchronous invocation.<br> 3. Extend / revise asynchronous support in AFCL.<br> 4. Develop asynchronous invokers for well-known FaaS systems.<br> 5. Develop *aSync xAFCL EE* to support nested asynchronous invocation of (base and compound) functions.<br> 6. Evaluate the *async xAFCL EE* with asynchronous serverless workflows.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
| Practical skills | Java, Python, Node.js, Cloud APIs.||
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


## *jFCfier* 

| Title | ***jFCfier*: Portable Java *FCfier*** |
| ----- | ----- | 
| Students | David Freina and Jonas Wagner | 
| Status | Development | 
| Description |  The goal of this thesis is to develop a portable Java FCfier (*jFCfier*), which allows the FC developer to annotate the target FaaS system per serverless function, faasifies parts of the Java monolith as serverless functions across multiple FaaS systems, updates the offloaded code with the corresponding API calls, converts Java monoliths as FCs, and evaluate their scalability. It is recommended to use the same annotation from our DAF tool (see our paper in the references).|
|Tentative tasks| 1. Develop a Java FCfier (*jFCfier*) for multiple FaaS systems.<br> 2. Compose / adapt a monolith that uses multiple cloud services.<br> 3. Code annotation (per line) in Java for FaaSification.<br> 4. Automatic package development and serverless function deployment of the faasified code.<br> 5. Evaluate the *jFCfier* with real-life serverless applications.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
|Practical skills | Java, Cloud APIs.||
---

## *xAFCLSim* 

| Title | ***xAFCLSim* simulation framework** |
| ----- | ----- | 
| Student | Mika Hautz | 
| Status | Final presentation | 
| Description | Running highly scalable FCs may be a long running and costly operation. To analyze the application behavior with minimal execution time and costs, users prefer to use simulation. The goal of this bachelor thesis is to develop an *xAFCL* simulation framework, which will simulate the FC execution. The simulated values will be calculated based on a novel FaaS computing model. A dynamism will be added based on some known distributions. FCs are built with the existing [Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012))] and run with the existing *xAFCL* enactment engine.|
|Tasks| 1. Compose / adapt a few real-life applications as FCs.<br> 2. Execute the composed FCs across multiple FaaS providers.<br> 3. Measure and profile the performance and cost of FCs.<br> 4. Model FCs and FaaS systems in *xAFCLSim*.<br> 5. Visualize the simulation.<br> 6. Evaluate the simulation (cost/performance/possibilities) with real execution.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless, AFCL | 
|Practical skills | Java||
---

## *xAFCLTrace* 

| Title | ***xAFCLTrace* scheduling and tracing framework** |
| ----- | ----- | 
| Student | Philipp Gritsch | 
| Status | Final presentation | 
| Description | Running FCs across a heterogeneous environment may not be reproducible, which affects the accuracy and estimation of the FC behavior. The goal of this thesis is to develop an *xAFCLTrace* scheduling and tracing framework, which will emulate the FC execution based on some scheduling algorithm. The traces may be generated by a real execution or by external sources. FCs are built with the existing Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012])) and run with the existing [xAFCL](https://github.com/sashkoristov/enactmentengine) enactment engine.|
|Tasks| 1. Compose / adapt a few real-life applications as FCs.<br> 2. Execute the composed FCs across multiple FaaS providers Log and trace the real FC execution.<br> 3. Develop a common interface AFCL -> Intermediary representation -> Scheduler (e.g., list-based) -> Intermediary representation -> Concrete Function Choreography Language (CFCL).<br> 4. Visualize the tracing.<br> 5. Evaluate various schedulers (cost/performance) with real execution.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless, AFCL | 
|Practical skills | Java.||
---


## *pyFCfier*

| Title | ***pyFCfier*: Portable Python FCifier** |
| ----- | ----- | 
| Student | Mark Nardi | 
| Status | Development | 
| Description |  The goal of this thesis is to develop a portable Python FCfier (*pyFCfier*), which allows the FC developer to select the target FaaS system per serverless function, faasifies parts of the monolith as serverless fynctions across multiple FaaS systems, updates the offloaded code with the corresponding API calls converts Python monoliths as FCs and evaluate their scalability.|
|Tasks| 1. Develop a Python FCifier *pyFCfier* for multiple FaaS systems.<br> 2. Compose / adapt a monolith that uses multiple cloud services.<br> 3. Code annotation (per line) in Python to be FaaSified.<br> 4. Automatic package development and serverless function deployment of the faasified code.<br> 5. Evaluate the *pyFCfier* with real-life serverless applications.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
|Practical skills | Python.||



Details for active bachelor theses can be found [here](./active/README.md).


# Closed bachelor theses

1. "A learning-based simulation framework for volatile cloud resources", Johannes Spies, Simon Triendl. SS2021.
1. "G2GA: Portable execution of workflows in Google Cloud Functions across multiple FaaS platforms", Anna Kapeller, Felix Petschko. SS2021.
1. "Decoupled Automatic Deployment of AFCL Workflows", Caroline Haller, Christoph Abenthung. SS2021.
1. "Establishing Virtual Networks in Amazon Web Services", Hüseyin Gündogan, WS2020.
1. "Function Choreography Scheduling Framework for Multiple FaaS Systems", Tobias Pockstaller, WS2020.
1. "Running workflow applications across multiple cloud providers", Marina Aichinger, SS2020
1. "Advisor for renting virtual machines from various public cloud service providers", Thomas Wurzer, SS2020
1. "Monitoring system for virtualized resources in a cloud data center", David Bucher, Peter Scheier, SS2020
1. "Middleware services to support workflow execution in a Multi-FaaS environment", Jakob Wallnöfer, SS2020, `Among top five theses for 2020` at the institute
1. High-level Modeling and Low-level Adaptation of Serverless Function Choreographies, Benjamin Walch, SS2020. [FCEditor](http://fceditor.dps.uibk.ac.at:8180/)
1. "Fault-tolerant execution of serverless functions across multiple FaaS systems", Matteo Bernard, Battaglin, SS2020. The initial version of [FTjFaaS] is integrated in [xAFCL](https://github.com/sashkoristov/enactmentengine/).
1. "Multi-layer enactment engine for workflow applications", Florian Maier, SS2020
1. "Enactment engine for composed serverless functions in Fission FaaS framework", Dominik Kuen, SS2020
1. "IoT Data analytics using Serverless Computing", Markus Reiter, Michael Kaltschmid, SS2020
1. "Fault-tolerant enactment engine for workflow applications on Amazon EC2 Spot Instances",	David Milic, Fabio Schett WS2019
1. "Scalable Data Analytics in Edge Cloud Continuum", Hanna Köb, WS2019
1. "Multi-provider enactment engine (EE) for serverless workflow applications", Jakob Nöckl, Markus Moosbrugger, SS2019. `Among top three theses for 2019` at the institute. Initial version of [xAFCL](https://github.com/sashkoristov/enactmentengine/).


Details for closed bachelor theses can be found [here](./closed/README.md).



----

# Contact

If you need any additional information, please do not hesitate to contact me on e-mail.

My topics for master theses may be found [here](https://github.com/sashkoristov/master-theses).