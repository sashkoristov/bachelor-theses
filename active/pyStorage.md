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