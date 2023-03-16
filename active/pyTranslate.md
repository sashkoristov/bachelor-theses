## *pyTranslate*

| Title | ***pyTranslate*: A Python Library for serverless workflows with interoperable OCR and translation cloud services ** |
| - | - | 
| Student | Elias Gendu | 
| Status | Requirements analysis | 
| Description | Switching between cloud providers can be a large investment. It often takes development time and cost to switch a provider. This thesis extends fService by implementing a Python library for abstracting OCR and translation cloud services of various cloud providers (e.g. ... of AWS and Google, respectively). The library will be evaluated with a real-life serverless workflow, whose functions can dynamically select on which cloud provider the services will be executed. Furthermore, the thesis will investigate various parameters that affect the optimal combination of providers for function, service, and input data location.
|Tasks| 1. Define interfaces and methods for the selected cloud services.<br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) and their abstracted services in Python. <br> 3. Build portable function choreography (*FC*) for a real-life application with dynamic inputs of serverless functions to specify the specific cloud service that they use (e.g. location of the input images).<br> 4. Integrate PyStorage for interoperable access to storages of AWS and Google.<br> 5. Evaluate the system with the developed FC and optimal selection of the proper cloud service.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Python; Cloud APIs.|
