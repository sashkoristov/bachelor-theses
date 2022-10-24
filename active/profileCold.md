## *profileCold*

| Title | ***profileCold*: Characterizing and modeling cold start overhead in federated FaaS** |
| ----- | ----- | 
| Student | Maximilian Gallinat  | 
| Status | Requirements analysis | 
| Description | The aim of this bachelor thesis is to conduct a series of experiments to characterize and profile numerous representative function implementations to analyze, model, and evaluate "cold start" effects. Cold start may be tested for various configurations (concurrency, assigned memory, package size, code size, number of files, layers, provider, region, programming language, caching, etc). The times for the functions are measured and the initial model will be created for the parameters that affect the cold start. Afterwards, the model will be evaluated for regions and functions for which no execution was conducted. The aim of this work is a better understanding of serverless computing for the very important cold start effect.|
|Tasks| 1. Define a list of parameters that can affect cold start in Function-as-a-Service (FaaS).<br> 2. Run benchmark experiments to learn impact of each parameter on at least two cloud providers (e.g., AWS and Google) and select the most important parameters per provider. <br> 3. Develop a mathematical model that estimates cold start overhead based on the selected parameters.<br> 4. Evaluate the model's inaccuracy with benchmark functions others than the one used for learning the model.|
| Theoretical skills | Cloud Computing, Serverless, AFCL. | 
| Practical skills | xAFCL; Cloud APIs.|
| Related work| 1. Many papers that analyzed cold start effect. E.g., check the related work in the [*xAFCL paper*](https://doi.org/10.1109/TSC.2021.3128137).|
