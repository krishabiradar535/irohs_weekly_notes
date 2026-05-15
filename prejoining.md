**Papers read before joining**

[Theoretically Principled Trade-off between Robustness and Accuracy](https://arxiv.org/pdf/1901.08573)

Previous research shows that there is tradeoff between accuracy and robustness, but that is undesirable.
It is very important to get this balance because we want to ensure that our model is able to predict correctly on normal data (accuracy) but also
want the predictons to remain stable even after perturbations (robustness). 
The paper introduces TRADES an adversarial training framework that finds a balance between accuracy and robustness.
TRADES involves 2 parts, an accuracy part and a robustness part, 
so it trains the model using these 2 terms by adding them together into a total loss and minimizing the final term so that we are able to get
good accuracy and robustness at the same time.

[Direct Preference Optimization](https://arxiv.org/pdf/2305.18290)
We want large language models to give us responses that align with "human preferences" (harmless, safe, etc). RLHF is one such method for 
training models to give safe responses. However, there are some issues with RLHF, the paper addresses them and proposes a simpler and better 
method called DPO (direct preference optimization).
DPO is much simpler because unlike RLHF it doesn't have an explicit reward model, it completely eliminates the RL optimization loop, but we still
achieve the goal of making our model generate "good answers" while not straying too much from the SFT dataset.

[MixAT: Combining Continuous and Discrete Adversarial Training for LLMs](https://arxiv.org/pdf/2505.16947)
There are two major ways of generating attacks, discrete attack generation and continuous attack generation. In discrete attacks prompts are 
modified using actual words or tokens, these are real prompts humans can type that can fool the model and hence are very dangerous. In continuous 
attacks instead of modifying the actual words we modify the embeddings by adding a small perturbation, this method is mathematically easy. 
The paper introduces MixAT, which combines the realism of discrete attacks and efficiency of continuous attacks. This way the attacks space is
widened and the model is able to resist a larger amount of attacks. 
