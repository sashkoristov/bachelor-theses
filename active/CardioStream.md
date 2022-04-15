## *CardioStream*

| Title | ***CardioStream*: Simulation of serverless real-time monitoring centre with streaming** |
| ----- | ----- | 
| Student | Andrei Amza | 
| Description | The goal of this bachelor thesis is to develop real-time monitoring centre of patients' sensor data with streaming. Simulation of real-time monitoring centre includes experiment setup, simulation, and evaluation phases. The set of actions should be performed in a form of event-based actions of the cloud provider (e.g., AWS) after streaming the patients' data. This includes serverless functions for noise intervals identification and elimination, heartbeat detection, detection of fibrillation, identification of segments and elevation, heart rate variability, statistical analysis and alerting. A smart scheduler will be developed to optimize cost-performance ratio by grouping multiple samples into a single message. The evaluation metrics will include measuring of response times for different test cases varying the workload (e.g., from 1K to 20K virtual patients ECG data simultaneously and their length). The experiment will be executed. The target is to measure speedup, cost, and throughput for various workload.|
|Tasks| 1. Develop and deploy serverless functions. <br> 2. Develop the event-based pipeline.<br> 3. Develop a smart scheduler.<br> 4. Evaluate *CardioStream* with various workloads (weak and strong scaling).|
| Theoretical skills | Cloud Computing, Serverless, file management, ECG data management (existing libraries). | 
| Practical skills | FaaS, Cloud API.|
| Related work | 1. https://kafka.apache.org/. <br> 2. https://aws.amazon.com/sqs/. <br> 3. https://aws.amazon.com/kinesis/. <br> 4. https://www.rabbitmq.com/.<br> 5. Hong, Sanghyun, Abhinav Srivastava, William Shambrook, and Tudor Dumitraș. "Go serverless: Securing cloud via serverless design patterns." In *10th USENIX Workshop on Hot Topics in Cloud Computing (HotCloud 18)*. 2018.|
---