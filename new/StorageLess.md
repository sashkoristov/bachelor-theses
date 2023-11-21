## *StorageLess*

| Title | ***StorageLess*: Benchmark networking of federated FaaS with federated storage infrastructure** |
| ----- | ----- | 
| Students | one or (ideally) two | 
| Description | Recently, we discovered several interesting observations regarding data transfers between serverless functions and cloud storage. First, although one would run the functions collocated with the storage, we determined that in many cases, especially for larger files, serverless functions would benefit if they access to storages in regions of other providers. The reason is that the general networking model is transefTime = latency + Size / Bandwidth. So, for larger files, the second part is large and can be significantly reduced with larger Bandwidth. Second observation is that the serverless functions achieve different bandwidth based on assigned memory, which also significantly affect its performance. In this thesis, students will run series of experiments across the globe to collect data and to create a "networking graph" of the federated cloud regions. The output will be to estimate transfer time for files from anywhere to anywhere in the world, based on the number of files and their size that are transferred. Students should use the existing benchmarking tool [TestOps](https://github.com/FaaSTools/testOps) (result of another bachelor thesis) to automatize experiments to collect data during various times and days of the week. The evaluation of the determined networking parameters will be executed with the existing *xAFCL* enactment engine ([xAFCL EE](https://github.com/sashkoristov/enactmentengine)) across several FaaS providers, based on the number of students and achieved initial measurements. For instance, ignore "very slow storages".
|Tasks| 1. Develop benchmarking functions that transfer files between FaaS and storages for different cloud providers. <br> 2. Develop scripts for TestOps for deployment and benchmarking of the existing serverless workflows in AFCL ([AFCL workflows](https://github.com/AFCLWorkflows/)).<br> 3. Run benchmarks with various *FCs* with various problem size and other important networking parameters. <br> 4. Determine empirical values for the parameters for retransmission *a* that multiplies latency and for bandwidth bottleneck *b* that multiplies bandwidth. E.g., the related work 4. showed values 10<*a*<15, and 0.8<*b*<1.<br> 5. Evaluate accuracy of the model for other functions that were not used for learning. <br> 6. (For two students) Apply the mathematical model in our simulator SimLess to be able to simulate executions of FCs without running them.|
| Theoretical skills | Cloud Computing, Serverless, workflow applications | 
| Practical skills | FaaS, Cloud API.|
| Related work | 1. *xAFCL* enactment engine with integrated simulator SimLess [*xAFCL EE*](https://doi.org/10.1109/TSC.2021.3128137). <br> 2. Various FaaS tools on our github organization [*FaaS Tools*](https://github.com/FaaSTools), such as GoDeploy and TestOps for automatic deployment and benchmarking. <br> 3. K. Fujiwara, H. Casanova, Speed and accuracy of network simulation in the SimGrid framework, ValueTools '07. Brussels, BEL, 1–10. <br> 4. H. Casanova et al. Versatile, scalable, and accurate simulation of distributed applications and platforms. J. Parallel and Distrib. Comput. 74, 10 (2014), 2899–2917  |
| Note | Students will achieve budget for running experiments on AWS and GCP. | 
---