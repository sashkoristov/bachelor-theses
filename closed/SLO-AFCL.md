## *SLO-AFCL*

| Title | ***SLO-AFCL*: FaaScinating resilience for function choreographies using service level objectives (SLOs)** |
| - | - | 
| Students | Julian Thöni and Benjamin Knjisa |
| Description |  ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) may run alternative *function deployments* (*FDs*) of a serverless workflow or function choreography (*FC*) in AFCL across the top five FaaS providers. It also can log various cost, performance, and fault tolerance parameters of functions and entire FCs. However, having a proactive component that will dynamically adapt which FDs and alternatives to run will improve its resilience. An example of SLO (service level objectives) for an FC would be minimum 99% of all executions will succeed, with maximum cost of 5$ and finish within 2 seconds. Thresholds may be failure rate of each function is maximum 0.5%. This bachelor thesis will adaptively determine which FD and which alternatives to run for each FC function based on specified SLOs, which can be defined for different parameters of functions (round trip time, cost, failure rate), for the FC (makespan, cost), for specific cloud region, and for different time period (in the last minute, hour, day, etc). *SLO-AFCL* can create and select new FDs in other cloud regions (twins), in the same cloud region with more or less memory (siblings), more FDs in parallel to increase availability, etc. *SLO-AFCL* will be evaluated with a real life workflow for various FaaS providers.
|Tasks| 1. Research parameters that can be used to define SLOs ranges and thresholds including parameters of functions, time periods, FC, cloud providers and their regions, etc.<br> 2. Develop interfaces with AFCL metadata DB.<br> 3. Develop / adapt monitoring for SLOs.<br> 4. Develop an AFCL adaptor that will adapt resource FDs and alternatives.<br> 5. Visualize SLO parameters.<br> 6. Evaluate *SLO-AFCL* with the real-life FC and specific scenarios that try to breach SLOs.|
| Theoretical skills | Cloud Computing, Serverless, AFCL, fault tolerance. | 
| Practical skills | Algorithms, Cloud APIs.|
| Related work | 1. [Google SRE](https://sre.google/). <br> 2. https://keptn.sh/.|

