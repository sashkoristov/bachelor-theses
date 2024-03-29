# *fOps*

## Details

| Title | ***fOps*: Automation in packaging, deployment, and testing of serverless functions in federated FaaS** |
| ----- | ----- | 
| Students | one or two | 
| Description |  The goal of this bachelor thesis is to develop a CI/CD pipeline for development, deployment, and functional testing of serverless functions across multiple providers. The main approach is to minimize the development effort and automatize the deployment and testing of the code for multiple FaaS providers (e.g., AWS, IBM, Google, Azure, Alibaba). The developer needs to develop the function locally only once (*function template*) and after pushing the code on git (eg. github), *fOps* pipeline will conduct a series of actions. First, *fOps* will encapsulate the code (*function implementation* - *FI*) for the selected programming language (e.g., Node.js, Go) for each supported FaaS provider. Second, *fOps* will deploy the code (FI) for each specified *function deployment* - *FD* (e.g. in MariaDB AFCL metadata database), which may include deploy the code on various cloud regions of multiple FaaS providers and determine the minimum needed memory, run the code with some predefined data inputs and test whether the code runs successfully on each FaaS provider. Finally, *fOps* stores deployment times, package size, resource link, and minimum memory in the existing AFCL metadata database for all FDs. *fOps* may consider to deploy multiple functions from a single code with multiple handlers and functions may be developed with fService and then also tests should check if the function may use all enumerated services. *fOps* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Develop a module for pipeline scripts. <br> 2. Develop wrappers for serverless function handlers for the selected programming language for various FaaS providers (e.g. AWS, IBM, Google, etc). <br> 3. Develop interfaces with AFCL metadata DB. <br> 4. Develop an automatic deployer for various FaaS providers (e.g. AWS, IBM, Google, etc).<br> 5. Evaluate *fOps* with real life applications.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Programming languages, Cloud APIs, git.|
| Related work | 1. Bachelor theses and tools [jfOps](https://github.com/FaaSTools/jfOps), `pyfOps`,  `pyFCfier`, `jFCfier`, [testOps](https://github.com/FaaSTools/testOps). <br> 2. (`Node.js FaaSifier`) S. Ristov, S. Pedratscher, J. Wallnöfer, and T. Fahringer, “DAF: Dependency-Aware FaaSifier for Node.js Monolithic Applications,” in IEEE Software, doi: 10.1109/MS.2020.3018334, [DAF](https://github.com/qngapparat/daf).<br> 3. (`Automatic function deployment`) [Terraform](https://www.terraform.io/).<br> 4. (`Automatic function deployment`) [Serverless](https://www.serverless.com/).<br>  5. (`Node2FaaS Framework`) [Node2FaaS *FCifier*](https://github.com/node2faas/framework).<br> 6. (`Automatic function deployment`) R. Cordingly, H. Yu, V. Hoang, Z. Sadeghi, D. Foster, D. Perez, R. Hatchett, and W. Lloyd. "The Serverless Application Analytics Framework: Enabling Design Trade-off Evaluation for Serverless Software." In 2020 21st ACM/IFIP International Middleware Conference: 6th International Workshop on Serverless Computing (WoSC'20). 2020, [SAAF](https://github.com/wlloyduw/SAAF). This tools can be used for wrappers and deployment scripts for various programming languages and FaaS providers.|
---


## Current status of fOps prototypes 

|  |**AWS** | **GCP** | **IBM Cloud** | **Azure Cloud** | **Alibaba Cloud** |
| :---: | :---: | :---: |:---: |:---: | :---: | 
| **Python** | ✅  | ❌ | ❌ | ❌ | ❌ |
| **Java**| ✅ |✅ |❌ |❌ | ❌ |
| **Go**| ❌ |❌ |❌ |❌ |❌ |
| **node.js** |  ❌ |❌ |❌ |❌ | ❌ |


