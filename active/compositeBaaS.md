## *compositeBaaS*

| Title | ***compositeBaaS*: An Ontology-Driven orchestration of BaaS-enabled AFCL serverless workflows ** |
| - | - | 
| Student | Rafael Mayer | 
| Status | Development | 
| Description | Cloud providers offer various BaaS (Backend-as-a-Service) services, such as translate natural languages or speech recognition. However, for more complex conversions, such as convert an english pdf into german speech, no BaaS service exists and users need to compose multiple BaaS services in a pipeline. In practice, this process is complex due to many constraints by the providers, such as available features of the specific BaaS service, or the limited problem size or throughput. The goal of this bachelor thesis is to create a system that facilitates the user in creating complex composition of BaaS services from the specified "intent" by the user, at the same time hiding implementation details and service- and provider-specific constraints from the user.|
|Tasks| 1. Building the ontology for composition of BaaS services, each wrapped in a separate serverless function.<br> 2. Implementat wrapper serverless functions for BaaS Services. <br> 3. Automatic generation of AFCL workflow based on BaaS intent and provider constraints and deployment of workflow functions.<br> 4. Evaluate the system with several BaaS services, such as speech-to-text and text-to-speech.|
| Theoretical skills | Cloud Computing, Serverless, abstractions. | 
| Practical skills | Cloud APIs, AFCL.|
