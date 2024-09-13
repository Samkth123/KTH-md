
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