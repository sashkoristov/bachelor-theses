## *CardioAFCL*

| Title | ***CardioAFCL*: Simulation of serverless real-time monitoring centre with AFCL workflows** |
| ----- | ----- | 
| Student | Katrin Antholzer | 
| Status | Requirements analysis | 
| Description | The goal of this bachelor thesis is to develop real-time monitoring centre of patients' sensor data using batch processing approach with AFCL. Simulation of real-time monitoring centre includes experiment setup, simulation, and evaluation phases. The set of actions should be performed in a form of an AFCL serverless workflow or function choreography (*FC*) after upload of patients' data. This includes serverless functions for noise intervals identification and elimination, heartbeat detection, detection of fibrillation, identification of segments and elevation, heart rate variability, statistical analysis, alerting, and reporting. A generator of a virtual patient ECG will be developed to simulate generated files. The evaluation metrics will include measuring of response times for different test cases varying the workload (e.g., from 1K to 20K virtual patients ECG data simultaneously and their length). The experiment will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)). The target is to measure speedup and throughput versus the number of cloud regions (<3 sec).
|Tasks| 1. Develop serverless functions. <br> 2. Develop AFCL FC that distributed the work.<br> 3. Evaluate *CardioAFCL* with various workload (weak and strong scaling).|
| Theoretical skills | Cloud Computing, Serverless, file management, ECG data management (existing libraries). | 
| Practical skills | FaaS, Cloud API.|
---