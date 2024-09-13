
### Abstract:
- ML on edge devices bring clear benefits ex improved reliability, latency and privacy.
- Also has challenges - other papers focus on resource bottleneck
- This paper focus on problems TinyML practitioners might have when operationalizing apps on edge devices.
	- Focus on monitoring and managing application, common functionality for MLOps platform - show how its made complicated by distributed nature of edge deployment.
	- Also issues that are unique to edge apps like protecting a models intellectual property and verifying its integrity.

### Introduction

TinyML - refers to use of ML models on resource constrained edge devices.
- attractive for smart home stuff, virtual assistnts, autonomus vehicles and smart surveillence
	- edge deployment can provide lower latency, more robustness and scalability and privacy compared to cloud deployment
- Challenges that hinder large scale edge AI use are
	- limited processing power of edge devices
	- Most of owrk in the field of TinyML focus on improve efficiency of models on resource constrained devices
	- This paper focus less on computational aspect
		- more focus on what challenges when ML put in production
		- No focus on ML model design or training
			- More focus on operational side
		- assume ML model is a deep neural network - but not limited to this
- Paper structured:
	- section II discussion on computational aspect of TinyML
	- section III discuss MLOps and introduce idea of TinyMLOps
	- section IV specific challenge ex dealing with fragmented device landscape
	- section V protecting intellectual property of ML model
	- section VI validate the result of a model
	- section VII conlude and give pointers for future work

### II - The computaional aspect of TinyML

Despite short history of TinyML, exists many techniques for reduce computational cost, memory footprint and energy consumption of ML models targeting edge deployment
- pruning
- model quantization
- knowledge distiallation
- adaptive computation
- automated neural architecture search
Some of these can only reach full potential if they have support of hardware platform they're deployed on

### III - MLOps and the need for TinyMLOps
Past decade, seen explosion of ML techniques applied in various domains.
These made ad-hoc and complicated, so hard to deploy in production. 85% of corporate AI initiatives struggle to move past test stages (estimation).

Even if estimation, you can say theat integration ML models in complex user facing apps reqire lots of forethought and continuous maintanence (especially if model updated over time with new data)

Technical dept exists - with ML its increased
- Addition to updating source code also need
- new training data
- better feature definitions
- hyper parameter settings
- new model architectures
All the above trigger update of application,

Also difficuly to:
- keep track of dependencies model has
- performance of model
- detect when it goes wrong
- detect when model is making potentially expensive mistakes

All the above give rise to MLOps - extension of devops

This paper argues for the extension of MLOps to TinyMLOps.
- Move form centralized cloud app to dexentralized edge based deployment
	- new challenges arise

##### A. Managing model versions
Centralizzed cloud based app
- sufficient to have single mode for all users (simply latest and greatest architecture for task at hand)
Decentralized edge based app
- model will be deployed on end users device
- different users have different devices with different computational resources, storage and network connectivity
- therefore instead of one model being trained need to support multiple models each with own computational cost and accuracy trade off
	- allows us to push smaller efficcient model to device with limited resources
	- or large more accurate to powerful devices
	- To complicate more, best model for given device depends on other factors as well, ex external factors.
		- if device connceted to charging point, energy consumption less of an issue, so a different model might be prefered depending on battery level.
		- Similarly depending on sitatuon, user might prefer slower accurate modelr
		- or faster less acurate model
		- or model that is fast to download on slow network compared to large model on wifi

Common technique for TinyML model optimiazation is reduced precision operations.
- traditionally NN require 32 bit numerical operations for training & evaluation
- but can do with 8,3,2, or even 1 (binary) weight and opretioans.
- training model more difficuly but has owrked with 4 bit weights.
- low precision operations do not however guarantee faster and more efficient models on all hardware platforms.
	- special supprot from hardware is needed to obtain an increased throughput or reduced energy consumption
	- as different hardware platforms support differnet set of operations and bit widths - we might need to develop different versions of a model each targeting specific platform

All examples above show that number of models that need to be managed by TinyMLOps system is much larger than numer of corresponeding on centralized deployment (==basically i cloud så har du ju bara ett environment, men på telefon,dator, osv.. allt som är edge är ju allting annorlunda och därflr svårare  att optimera gentemot den plattformen==)

##### B. Observability

ML models used increasingly in consumer facing applications - monitoring and observability are key to ensuring model keeps performing as expected

Relatively straight forward to implement model observability on cloud platform as all input data is centralized.

Less trivial if model is deployed on edge

Benefit of edge deployment is that no data needs to leave device, which provides stronger privacy guarantees than cloud processing
- argument would be rendered invalid if periodically shared data with cloud for analyssi and re-training
- could record basic statistics locally and share with cloud anonymously but depends on app if its useless or not
- also interested in monitoring number of requests user has made and the execution time of model.
	- Different users have different hardware platforms with different computational resources - its interesting to record actual execution time, memory and energy consumption on end user device
	- These telemtry data can signal performance issues that might neccessitate further perofrmance optimizations of the model.
	- Store this info locally then give to cloud anonymously when connected to wifi and user gives permissoin.
	- All this needs to be considered with implementing ==TinyMLOps observability functionality==


##### C. Pay-per-query business model
Common business model for ML apps is pay per query. EX Google cloud vision API charge 1,5dollars per 1000 requests for tasks such as face detection.

Similar to observability, this is trivial to implement on cloud as all API are processed at the samt endpoint.

Even though end-user carries computational cost of model inference, the app developer still needs to be compensated for cost of developing and training a model.

THis is hard to do on model that is replicated on a large number of end users devices that might not even be connected to internet.
- Instead, could offer prepaid packages where user purchases the right to perform certain number of model calls.
- The app has to keep track of how many requests user has executed and will deny access if this exceeds the number of requests the user has paid for. ==Doing this in a secure offline way on untrusted hardware is not trivial and would be very useful feature for a TinyMLOps solution==

##### D. Retraining and personalizing models

Modern ML apps are not static anymore, they are updated continuously as new data has been observed.

On cloud, this is computationally expensive but still easy as all is centralized

Edge-based, it is far from trivial

Major benefit of edge based app is that data stays on local device
- attractive form privacy point of view
- also means though its impossible to centralize data to train new models without invalidating privacy argument
- Instead, have to rely on Federated Learning to update the model

==Federated Learning===
- a user downloads the current model and updates it locally with his own data
- The updates to the model are sent to the cloud where it is averaged with out users updates to improve the shared model
- Periodically, the updated global model is pushed to each device, allowing invidual user to benefit from the experience of the model on other devices.
- Fedarated learning is not a trivial problem as heteregenous data generated by differnet clients cause the local models to diverge, making it difficult to aggregate the local updates to a global update.
- Despite new in research, Federated Learning is already deployed in practice

Several challenges arise when implementing Federated Learning on TinyML setting. First is computational cost.
- We rely on edge device to calculate model updates instead of performing inference using trained model, the computaational cost increases accordingly.
- In addition, model updates need to be shared to the cloud backend periodically.
	- This has direct impact on energy consumption of the application
		- Could be possible to store some of the data locally and calculate the model updates when the device is idle or connected to a charger

Most Federated Learning approaches make assumption that labelled data is available. This might be realistic in certain settings such as medical use where doctors annotate medical records but nor realistic for TinyML setting. Even if user can be asked to provide label its most likely low quality.
- Several techniques have been developed that can use unlabelled local data to improve glbal model either in semi supervised or unsupervised way.

We do not either need to necessarily aggregate all local updates to the model into the global model.
- By deploying model to edge device, model will usually only process data belonging ot a single usr or generated in a single location.
- This can be exploited to triain specialized models that are overfitted to s specific user or location
- ex could be peronsalized auto complete functionality or anomaly detection model trained for predictive maintenece of tine learns characteristics of single machine or sensor

==Kritki av oss? A/B testing?==

### IV. Targeting a Fragmented IoT Landscape

Cloud infrastructure for ML tasks is uniform
- Usually high end Linux servers equipped with NVIDIA hardware accelerators
- Edge landscape is however much more fragmented with a wide range of different devices from different vendors, each with different software support and hardware capabilities.
- There is currently a trend towards custom hardware accelerators that support ML applications in more energy efficient ways, which in turn makes it so that fragmentation will only increase in the future.
- ==Clearly, this is a major challenge for a TinyMLOps platform==










































