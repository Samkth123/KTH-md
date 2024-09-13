
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






























