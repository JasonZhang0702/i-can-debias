# coco_debiasing_neuron
This repository is used to reproduce the experimental results of
_**Uncovering Neuronal Mechanisms of Intrinsic Self-Debiasing in Large Language Models via Contrastive Learning**_, 
and meanwhile, it supplements the details that are not described clearly in the paper. I hope it can help and inspire you.

## Our Framework
![framework1.jpg](figure%2Fframework1.jpg)

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

## Research Questiones and Results

#### RQ1: Can deactivating $COCO$ neurons impair LLMs' unbiased response capability more significantly than baseline neuron extraction strategies?
![RQ1.png](figure%2FRQ1.png)
- Our analysis reveals a striking pattern: deactivating COCO neurons leads to a statistically significant decline in the LLMs’ unbiased response capability.

---


#### RQ2: Can the linear and nonlinear neuron enhancement editing proposed herein significantly improve LLMs' performance on both bias and general capability benchmarks? And does this effect generalize consistently across different LLMs?
![RQ2.png](figure%2FRQ2.png)
- Both enhancement strategies effectively improve the unbiased response capability of their target models.
- Enhancement editing improves models’ truthfulness and deep reasoning but impairs knowledge representation.
- The linear and nonlinear enhancement strategies lack consistency and generalizability

---

#### RQ3: Can neuron-edited LLMs maintain stable unbiased responses under adversarial scenarios with injected jailbreak prompts? And this can validate the robustness of enhancement strategies?
![RQ3.png](figure%2FRQ3.png)
- Our neuron enhancement strategy effectively resists safety jailbreak prompt injection attacks and boosts model robustness.

---

#### RQ4: How do the proposed neuron editing enhancement strategies alter LLMs’ internal attention distribution patterns compared to unedited models? And can these alterations offer intrinsic interpretability for LLMs’ bias mitigation behavior?
![RQ4.png](figure%2FRQ4.png)
- Attention shifts from enhancement editing exhibit high sparsity and notable focus on sequence start and end.

