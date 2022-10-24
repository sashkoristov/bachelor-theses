## *GoSpeechLess*

| Title | ***GoSpeechLess*: An interoperable library for serverless functions in Go to convert speech and text** |
| - | - | 
| Students | David Meyer | 
| Status | Requirements analysis | 
| Description | Development of serverless functions that use multiple cloud services is a complex task as it may require huge development effort to integrate various libraries for each cloud service that the function uses. This bachelor thesis extends *fService* to support programming language Go and various cloud services (e.g., speech2text and text2speech) of multiple cloud providers (e.g., AWS, Google, etc). Heuristics may be added to determine which specific cloud service to be used (e.g., Amazon Transcribe or Google SpeechtoText) based on the storage location of the audio file.
|Tasks| 1. Define interfaces and methods for the selected cloud storages. For instance, voice2text(sourceAudio, destText).<br> 2. Develop implementations of interfaces for various cloud providers (e.g., AWS, Google, etc) and their abstracted services in Go. <br> 3. Build portable function choreography (*FC*) for a real-life application with dynamic inputs of serverless functions to specify the specific cloud service that they use (e.g. location of the input audio files).<br> 4. Integrate GoStorage for interoperable access to storages of AWS and Google.<br> 5. Evaluate the system with the developed FC and optimal selection of the proper cloud service.|
| Theoretical skills | Cloud Computing, Serverless. | 
| Practical skills | Go; Cloud APIs.|
| Related work| 1. B. Hackstock, "fService: Configurable abstraction for serverless development", Bachelor thesis, WS2021. [details](./closed/fService.md).<br> 2. "*portableGo*: Portable development and deployment of Go functions in serverless workflows", Simon Brandacher. SS2022. [details](./closed/portableGo.md).<br>3. [GoDeploy](https://github.com/FaaSTools/GoDeploy). S. Ristov, S. Brandacher, M. Felderer, R. Breu, “GoDeploy: Portable Deployment of Serverless Functions in Federated FaaS”, accepted on IEEE Cloud Summit 2022, Fairfax, Virginia, USA, Oct. 2022. (https://www.ieeecloudsummit.org/2022-program)|

