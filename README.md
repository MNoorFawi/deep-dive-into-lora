## Introduction

In the evolving landscape of large language models (LLMs) and the almost infinite number of use cases that they can help in, the ability to fine-tune them efficiently and effectively stands out as a challenge especially with both limited resources and data. This is where [Low-Rank Adaptation (LoRA)](https://huggingface.co/papers/2106.09685) technique appeared to be a game-changer enabling fine-tuning very big LLMs to specific task on limited resources and datasets.

LoRA introduces a seemingly-simple yet powerful and cost-effective way to fine-tune LLMs and adapt them to a specific task by integrating low-rank matrices into the model's architecture. Put simple, instead of retraining the whole model's parameters over our data, we identify specific layers in the model's architecture that we would like to tweak and adjust and represent their weight matrices with smaller matrices and retrain these smaller ones instead in a parameter-efficient way. This approach significantly reduces the number of trainable parameters but still enable the base model to adapt to a specific task efficiently.

In this blog post, we will delve deep into how LoRA works under the hood, looking at its mathematical foundations by walking through a practical example. By the end of this post, you'll see how useful and necessary LoRA is when it comes to fine-tuning large language models.
