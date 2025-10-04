# coco_debiasing_neuron


## Abstract: 
Bias is a key behavioral characteristic of large language models (LLMs) that deviates from factuality. 
Enhancing and interpreting the debiasing behavior of LLMs is crucial for building safe and trustworthy AI systems. 
However, existing studies still leave a notable gap regarding the internal neuronal regulatory mechanisms underlying LLMs’ debiasing behavior. 
To address this gap, we leverage a contrastive learning paradigm to identify critical neurons from the reasoning hidden states of LLMs and these neurons exhibit significant internal consistency and external differentiation in their activation patterns between biased and unbiased scenarios. 
These neurons are highly sensitive to biases in specific scenarios and account for less than 1\% of the total parameters. 
Selective deactivation of these neurons significantly reduces the LLMs’ unbiased response rate to below 10\%. 
To enhance debiasing capability, we introduce two neuron editing strategies tailored for linear and nonlinear debiasing systems, respectively. 
Experimental results show that our linear enhancement elevates the unbiased response rate of Llama3 to nearly 90\% with a maximum gain exceeding 50\%, while nonlinear enhancement improves Mistral-7B’s unbiased response rate by an average of 10\% with a maximum gain over 23\%. 
Generalization experiments demonstrate that the enhanced LLMs not only exhibit stronger robustness against safety jailbreak prompt injection attacks but also show varying degrees of improvement in factuality and reasoning ability. 
Finally, we interpret the intrinsic logic of the LLMs’ debiasing behavior from the perspective of attention mechanisms and reveal the high sparsity and specific positional focus of attention shifts during the debiasing process.


