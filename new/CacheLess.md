## *CacheLess*


| Title | ***CacheLess*: Cache-aware data flow in AFCL serverless workflows** |
| ----- | ----- | 
| Students | one or two | 
| Description | Functions that are orchestrated in a serverless workflow or *function choreography* (*FC*) usually pass data through files using storage. However, if the successor function runs in the same container as the predecessor, then the file will be already present inside the file system of the function. This will be possible if both functions of the workflow run the same resource, i.e., have the same Amazon Resource Name (ARN). The goal of this bachelor thesis is to investigate for which serverless workflows would be beneficial to create a single deployment package for all functions so that the same resource is called and to have always warm start. This approach may cause increased start time of the function, but reduces data movement as data will be already in the container and no need to be downloaded and uploaded. Also, the number of warm starts should increase (probably for single functions only, but not for loops). (in case of two students: A mathematical model will be created to determine the size of the parallel loop to optimize the execution. This model should determine the tradeoff between caching files in the containers and warm starts vs. higher scalability, but with cold start). The experiments will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) across two FaaS providers (e.g., AWS and GCP).
|Tasks| 1. Develop several benchmark serverless functions on at least two cloud providers (e.g., AWS and GCP) that exchange files. <br> 2. Develop serverless workflows in AFCL (or use existing [AFCL workflows](https://github.com/AFCLWorkflows/)).<br> 3. Evaluate various *FCs* with various problem size and other important parameters. <br> 4. (For two students) Create a matematical model for the function round trip time and workflow makespan.<br> 5. (For two students) Evaluate accuracy of the model. <br> 6. (For two students) Apply the mathematical model in our simulator SimLess to be able to simulate executions of FCs without running them.|
| Theoretical skills | Cloud Computing, Serverless, workflow applications | 
| Practical skills | FaaS, Cloud API.|
| Related work | 1. *xAFCL* enactment engine with integrated simulator SimLess [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137). <br> 2. Various FaaS tools on our github organization [*FaaS Tools*](https://github.com/FaaSTools), such as GoDeploy and TestOps for automatic deployment and benchmarking. |
| Note | Student will achieve budget for running experiments on AWS and GCP. | 
---