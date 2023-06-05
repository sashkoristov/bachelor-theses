## *PySpeechLess*

| Title | ***PySpeechLess*: Interoperable Python serverless functions in federated FaaS** |
| - | - | 
| Students | Lukas Pernter and Simon Muscatello | 
| Status | Development | 
| Description | Cloud users tend to be able to freely move their applications and select backend managed cloud service services from various cloud providers in Federated FaaS, which may provide significant benefits in terms of performance, quality of service, and costs. Unfortunately, portability and interoperability usually require considerable development effort. To bridge this gap,  this bachelor thesis will develop PySpeechLess, a Python library that abstracts the speech-to-text and text-to-speech functionalities offered by different cloud providers, such as AWS and Google. With PySpeechLess, developers can code portable serverless functions that can use interoperable managed cloud services. The performance of PySpeechLess will be evaluated with a practical serverless workflow. This workflow enables functions to dynamically choose the most suitable cloud provider, region and scaling in terms of memory and performance tiers within a single cloud provider. Additionally, the thesis will explore all kinds of various parameters that impact the optimal combination of providers for function execution, such as service delivery, accuracy, cost, performance, based on function and data location.
|Tasks| 1. Define interfaces and methods for the selected cloud services.<br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) and their abstracted services in Python. <br> 3. Build portable function choreography (*FC*) for a real-life application with dynamic inputs of serverless functions to specify the specific cloud service that they use (e.g. location of the input audio files).<br> 4. Integrate PyStorage for interoperable access to storages of various providers (e.g., AWS and Google).<br> 5. Evaluate PySpeechLess with the developed FC and optimal selection of the proper cloud service.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Go; Cloud APIs.|
| Related work| 1. B. Hackstock, "fService: Configurable abstraction for serverless development", Bachelor thesis, WS2021. [details](./closed/fService.md).

