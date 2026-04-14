## gemma+DPO

### basic info
**gemma 4 models:**
Gemma is a family of generative artificial intelligence models and you can use them in a wide variety of generation tasks, including question answering, summarization, and reasoning. Gemma models are provided with open weights and permit responsible commercial use, allowing you to tune and deploy them in your own projects and applications.

Gemma 4 model family spans three distinct architectures tailored for specific hardware requirements:

Small Sizes: 2B and 4B effective parameter models built for ultra-mobile, edge, and browser deployment (e.g., Pixel, Chrome).
Dense: A powerful 31B parameter dense model that bridges the gap between server-grade performance and local execution.
Mixture-of-Experts: A highly efficient 26B MoE model designed for high-throughput, advanced reasoning.
You can download Gemma 4 models from Kaggle and Hugging Face. For more technical details on Gemma 4, see the Model Card. Earlier versions of Gemma core models are also available for download. For more information, see Previous Gemma models.

Direct Preference Optimization (DPO): Training a model using preference data. For a single prompt, you provide a "chosen" (good) response and a "rejected" (bad) response. The model learns to increase the probability of the chosen response and decrease the probability of the rejected one. This directly targets negative constraints, teaching the model exactly what to avoid.
