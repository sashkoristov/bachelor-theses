# bachelor-theses
Repository for available, active and closed topics for Bachelor theses in the context of the class “Seminar mit Bachelorarbeit”


As a result of several bachelor and master theses that I supervised, as well as our own research, we have developed a prototype of the *xAFCL* enactment engine, which is able to run serverless workflows or function choreographies (*FCs*) across many widely-known cloud providers (AWS Lambda, IBM Cloud Functions, Google Cloud Functions, Alibaba Function Compute, Microsoft Azure Cloud Functions, etc.)

The following paragraphs present the available and recently started bachelor theses directly connected with the AFCL Environment.


# Available bachelor theses

The following topics for bachelor theses are available for the summer semester 2021:
* Tentative start February-March 2021
* Tentative finish June-December 2021


## 1. Portable Java *FCfier*

| Title | **Portable Java *FCifier*** |
| ----- | ----- | 
| Description |  The goal of this thesis is to develop a portable Java *FCfier*, which allows the FC developer to select the target FaaS system per serverless function, faasifies parts of the Java monolith as serverless fynctions across multiple FaaS systems, updates the offloaded code with the corresponding API calls, converts Java monoliths as FCs, and evaluate their scalability. It is recommended to use the same annotation of our DAF tool (see our paper in the references).
|Tasks| 1. Develop a Java FCifier for multiple FaaS systems.<br> 2. Compose / adapt a monolith that uses multiple cloud services.<br> 3. Code annotation (per line) in Java to be FaaSified.<br> 4. Automatic package development and serverless function deployment of the faasified code.<br> 5. Evaluate the *FCifier* with real-life serverless applications.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
|Practical skills | Java, Cloud APIs.|
|References| 1. (`FaaSification annotation`) S. Ristov, S. Pedratscher, J. Wallnöfer, and T. Fahringer, “DAF: Dependency-Aware FaaSifier for Node.js Monolithic Applications,” in IEEE Software, doi: 10.1109/MS.2020.3018334, [DAF](https://github.com/qngapparat/daf).<br> 2. (`Portable invocation`) Middleware services to support workflow execution in a Multi-FaaS environment student: Jakob Wallnöfer, supervisor: Sashko Ristov, [js2faaS](https://github.com/qngapparat/js2faas), [java2faaS](https://github.com/qngapparat/java2faas), [X2FaaS](https://github.com/qngapparat/X2FaaS).<br> 3. (`Automatic function deployment`) R. Cordingly, H. Yu, V. Hoang, Z. Sadeghi, D. Foster, D. Perez, R. Hatchett, and W. Lloyd. "The Serverless Application Analytics Framework: Enabling Design Trade-off Evaluation for Serverless Software." In 2020 21st ACM/IFIP International Middleware Conference: 6th International Workshop on Serverless Computing (WoSC'20). 2020, [SAAF](https://github.com/wlloyduw/SAAF).<br> 4. (`Automatic function deployment`) [Terraform](https://www.terraform.io/).<br> 5. (`Node2FaaS Framework`) [Node2FaaS *FCifier*](https://github.com/node2faas/framework).<br> 6. (Podilizer)[https://github.com/serviceprototypinglab/podilizer]. | |
---

## 2. jContainer (or PyContainer or jsContainer)

| Title | **jContainer: Portable Execution of Serverless Functions in container systems** |
| ----- | ----- | 
| Description | All widely-known FaaS systems set up many design limitations (code size or memory assignment) and runtime limitations (size of input / output data, function duration, or hard disk size). The goal of this thesis is to develop a portable Java `jContainer` tool (or Python `PyContainer` or Node.js `jContainer`), which allows portable execution of serverless functions in multiple container systems, e.g., AWS Fargate or ECS. You may see our jFaaS too for portable execition of serverless functions on all widely-known FaaS system. 
|Tasks| 1. Develop a Java `jContainer` for multiple FaaS systems.<br> 2. Compose / adapt a real-life application that uses multiple cloud services.<br> 3. Integrate `jContainer` in AFCL.<br> 4. Automatic container development and serverless function deployment of the serverless function.<br> 5. Evaluate the `jContainer` with the real-life serverless applications across multiple container systems.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Container Systems | 
|Practical skills | Java (or Python, Node.js), Cloud APIs.|
|References| 1. (jFaaS)[https://github.com/sashkoristov/jFaaS].<br> 2. (`Automatic function deployment`) R. Cordingly, H. Yu, V. Hoang, Z. Sadeghi, D. Foster, D. Perez, R. Hatchett, and W. Lloyd. "The Serverless Application Analytics Framework: Enabling Design Trade-off Evaluation for Serverless Software." In 2020 21st ACM/IFIP International Middleware Conference: 6th International Workshop on Serverless Computing (WoSC'20). 2020, [SAAF](https://github.com/wlloyduw/SAAF).<br> 3. (`Automatic function deployment`) [Terraform](https://www.terraform.io/).<br> 4. (`Node2FaaS Framework`) [Node2FaaS *FCifier*](https://github.com/node2faas/framework).<br> 5. Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012))] | |
---


Develop invokers to other compute end points - e.g. AWS ECS, Fargate, Docker, Kubernetes, Fission, OpenWhisk ... This will allow xAFCL to run not only serverless functions, but also functions in a container and on some open source FaaS frameworks.

## 3. AFCL vs-code IntelliSense

Initial idea: build the FC using VS-code, but with intelligent proposal to fill the code (IntelliSense).


# Recently started bachelor theses for the AFCL Environment)

## 1. *xAFCL* simulation framework

| Title | ***xAFCL* simulation framework** |
| ----- | ----- | 
| Student | Mika Hautz | 
| Status | Requirements analysis | 
| Description | Running highly scalable FCs may be a long running a costly operation and in order to mitigate costs, users prefer to use simulation. The goal of this thesis is to develop an *xAFCL* simulation framework, which will simulate the FC execution. The simulated values will be calculated based on a novel computing model. FCs are built with the existing [Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012))] and run with the existing *xAFCL* enactment engine.
|Tasks| - Compose / adapt a few real-life applications as FCs - Execute the composed FCs across multiple FaaS providers Measure and profile the performance and cost of FCs. Model FCs and FaaS systems in the AFCL Environment simulation framework. Visualize the simulation. Evaluate the simulation (cost/performance/possibilities) with real execution.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
|Practical skills | Java|
|References| 1. S. Ristov, S. Pedratscher, T. Fahringer, “AFCL: An Abstract Function Choreography Language for serverless workflow specification,” Future Generation Computer Systems, Volume 114, 2021, Pages 368-382, ISSN 0167-739X, https://doi.org/10.1016/j.future.2020.08.012. Enactment engine to run serverless workflows https://github.com/sashkoristov/enactmentengine. A multi-FaaS toolkit to facilitate development of portable applications https://github.com/sashkoristov/jFaaS| |
---

## 2. *xAFCL* scheduling and tracing framework

| Title | ***xAFCL* scheduling and tracing framework** |
| ----- | ----- | 
| Student | Philipp Gritsch | 
| Status | Requirements analysis | 
| Description | Running FCs across such a heterogeneous environment may not be reproducible, which affects te accuracy and estimation of the FC execution. The goal of this thesis is to develop an *xAFCL* scheduling and tracing framework, which will emulate the FC execution based on some schedling algorithm. The traces may be generated by a real execution or by external source. FCs are built with the existing [Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012))] and run with the existing *xAFCL* enactment engine.
|Tasks| 1. Compose / adapt a few real-life applications as FCs.<br> 2. Execute the composed FCs across multiple FaaS providers Log and trace the real FC execution.<br> 3. Develop a common interface AFCL -> Intermediary representation -> Scheduler (e.g., list-based) -> Intermediary representation -> Concrete Function Choreography Language (CFCL).<br> 4. Visualize the tracing.<br> 5. Evaluate various schedulers (cost/performance) with real execution.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless, AFCL | 
|Practical skills | Java.|
|References| 1. S. Ristov, S. Pedratscher, T. Fahringer, “AFCL: An Abstract Function Choreography Language for serverless workflow specification,” Future Generation Computer Systems, Volume 114, 2021, Pages 368-382, ISSN 0167-739X, https://doi.org/10.1016/j.future.2020.08.012.<br> 2. Enactment engine to run serverless workflows https://github.com/sashkoristov/enactmentengine. <br> 3. A multi-FaaS toolkit to facilitate development of portable applications https://github.com/sashkoristov/jFaaS| |
---


## 3. Portable Python FCifier

| Title | **Portable Python FCifier** |
| ----- | ----- | 
| Student | Mark Nardi | 
| Status | Requirements analysis | 
| Description |  The goal of this thesis is to develop a portable Python FCfier, which allows the FC developer to select the target FaaS system per serverless function, faasifies parts of the monolith as serverless fynctions across multiple FaaS systems, updates the offloaded code with the corresponding API calls converts Python monoliths as FCs and evaluate their scalability. 
|Tasks| 1. Develop a Python FCifier for multiple FaaS systems.<br> 2. Compose / adapt a monolith that uses multiple cloud services.<br> 3. Code annotation (per line) in Python to be FaaSified.<br> 4. Automatic package development and serverless function deployment of the faasified code.<br> 5. Evaluate the *FCifier* with real-life serverless applications.|
| Theoretical skills |  Distributed Systems, Cloud Computing, Serverless | 
|Practical skills | Python.|
|References| 1. (`FaaSification annotation`) S. Ristov, S. Pedratscher, J. Wallnöfer, and T. Fahringer, “DAF: Dependency-Aware FaaSifier for Node.js Monolithic Applications,” in IEEE Software, doi: 10.1109/MS.2020.3018334, [DAF](https://github.com/qngapparat/daf).<br> 2. (`Portable invocation`) Middleware services to support workflow execution in a Multi-FaaS environment student: Jakob Wallnöfer, supervisor: Sashko Ristov, [js2faaS](https://github.com/qngapparat/js2faas), [java2faaS](https://github.com/qngapparat/java2faas), [X2FaaS](https://github.com/qngapparat/X2FaaS).<br> 3. (`Automatic function deployment`) R. Cordingly, H. Yu, V. Hoang, Z. Sadeghi, D. Foster, D. Perez, R. Hatchett, and W. Lloyd. "The Serverless Application Analytics Framework: Enabling Design Trade-off Evaluation for Serverless Software." In 2020 21st ACM/IFIP International Middleware Conference: 6th International Workshop on Serverless Computing (WoSC'20). 2020, [SAAF](https://github.com/wlloyduw/SAAF).<br> 4. (`Automatic function deployment`) [Terraform](https://www.terraform.io/).<br> 5. (`Node2FaaS Framework`) [Node2FaaS *FCifier*](https://github.com/node2faas/framework).| |



# Active bachelor theses

* "A learning-based simulation framework for volatile cloud resources", Johannes Spies, Simon Triendl. Status - Initial Presentation
* "Decoupled Automatic Deployment of AFCL Workflows", Caroline Haller, Christoph Abenthung. Status - Finalizing development.
* "Function Choreography Scheduling Framework for Multiple FaaS Systems", Tobias Pockstaller. Status - Writing the thesis.
* "G2GA: Portable execution of workflows in Google Cloud Functions across multiple FaaS platforms", Anna Kapeller, Felix Petschko. Status - Development.

Details for active bachelor theses can be found [here](./active/readme.md).


# Closed bachelor theses

* "Advisor for renting virtual machines from various public cloud service providers", Thomas Wurzer, SS2020
* "Monitoring system for virtualized resources in a cloud data center", David Bucher, Peter Scheier, SS2020
* "Middleware services to support workflow execution in a Multi-FaaS environment", Jakob Wallnöfer, SS2020, `Among top five theses for 2020` at the institute
* High-level Modeling and Low-level Adaptation of Serverless Function Choreographies, Benjamin Walch, SS2020. [FCEditor](http://fceditor.dps.uibk.ac.at:8180/)
* "Fault-tolerant execution of serverless functions across multiple FaaS systems", Matteo Bernard, Battaglin, SS2020. The initial version of [FTjFaaS] is integrated in [xAFCL](https://github.com/sashkoristov/enactmentengine/).
* "Multi-layer enactment engine for workflow applications", Florian Maier, SS2020
* "Enactment engine for composed serverless functions in Fission FaaS framework", Dominik Kuen, SS2020
* "IoT Data analytics using Serverless Computing", Markus Reiter, Michael Kaltschmid, SS2020
* "Fault-tolerant enactment engine for workflow applications on Amazon EC2 Spot Instances",	David Milic, Fabio Schett WS2019
* "Scalable Data Analytics in Edge Cloud Continuum", Hanna Köb, WS2019
* "Multi-provider enactment engine (EE) for serverless workflow applications", Jakob Nöckl, Markus Moosbrugger, SS2019. `Among top three theses for 2019` at the institute. Initial version of [xAFCL](https://github.com/sashkoristov/enactmentengine/).


Details for closed bachelor theses can be found [here](./closed/readme.md).



----

# Contact

If you need any additional information, please do not hesitate to contact me on sashko@dps.uibk.ac.at.