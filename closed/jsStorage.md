## *jsStorage*

| Title | ***jsStorage*: Interoperable data access in federated storage infrastuctures** |
| - | - | 
| Students | Felix Heine and Maximilian Heine | 
| Description | Cloud users tend to be able to freely move their applications and select cloud storage from various cloud providers in Federated FaaS, which may provide significant benefits in terms of performance, quality of service, and costs. Unfortunately, portability and interoperability usually require considerable development effort to apply SDKs of various storage providers. To bridge this gap,  this bachelor thesis will develop jsStorage, a node.js library that abstracts the storages by different cloud providers, such as AWS and Google. With jsStorage, developers can code portable serverless functions that can access federated storage infrastuctures. The performance and benefits of jsStorage will be evaluated with a practical serverless workflow and an existing FaaSifier. Additionally, the thesis will explore the parameters of federated storage infrastructure, such as bandwidth and latency between cloud regions.
|Tasks| 1. Define interfaces and methods for the selected cloud providers (e.g., copy file or create bucket).<br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) and their abstracted storages in node.js. <br> 3. Integrate jsStorage in the M2FaaS FaaSifier.<br> 4. Build portable functions that use jsStorage.<br> 5. Evaluate jsStorage and explore parameters of federated storage infrastructure.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | node.js; Cloud APIs.|
