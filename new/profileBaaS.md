## *profileBaaS*


| Title | ***profileBaaS*: Characterizing and profiling Backend-as-a-Service in Federated FaaS ** |
| ----- | ----- | 
| Students | one or two | 
| Description | The aim of this bachelor thesis is to conduct a series of experiments to characterize and profile numerous function implementations of serverless applications represented as functions choreographies (FCs) that use cloud services Backend-as-a-Service (BaaS). FCs may be tested for various configurations (concurrency, assigned memory, latency, region, programming language, restriction etc). The times for the functions and FCs are measured with white and black box testing and then evaluated. The measured data is stored in a database and then statistically evaluated and visualized. The aim of this work is a better understanding of serverless computing for different FCs, FaaS, and BaaS. The trade-off between performance and costs of the same service offered by different providers will be examined more closely. Additionally, possibility to run BaaS services directly without wrapping them in FaaS will be considered. The experiment will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)).
|Tasks| 1. Develop serverless functions on at least two cloud providers (e.g., AWS and Google) that use interoperable access to cloud service of different providers (e.g. OCR, Text2Speech, Digital Twins, cloud storage, ...). <br> 2. Develop FCs in AFCL.<br> 3. Evaluate *FCs*, BaaS, and FaaS with various workload (weak and strong scaling). <br> 4. (If two students) Create a matematical model for the selected BaaS services for twins and siblings (see my [SimLess paper](https://doi.org/10.1145/3542929.3563478)). Apply this model in SimLess to be able to simulate without measuring the BaaS services.|
| Theoretical skills | Cloud Computing, Serverless | 
| Practical skills | FaaS, Cloud API.|
| Related work | 1. *xAFCL* enactment engine [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137). <br> 2. Abstract Function Choreography Language ([AFCL](https://doi.org/10.1016/j.future.2020.08.012)). <br> 3. Various FaaS tools on our github organization [*FaaS Tools*](https://github.com/FaaSTools). |
| Note | Student will achieve budget for running experiments on AWS and Google. | 
---
