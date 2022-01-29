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