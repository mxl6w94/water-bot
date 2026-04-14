# gemma+DPO

### basic info
**gemma 4 models:**
Gemma is a family of generative artificial intelligence models and you can use them in a wide variety of generation tasks, including question answering, summarization, and reasoning. Gemma models are provided with open weights and permit responsible commercial use, allowing you to tune and deploy them in your own projects and applications.

Gemma 4 model family spans three distinct architectures tailored for specific hardware requirements:

Small Sizes: 2B and 4B effective parameter models built for ultra-mobile, edge, and browser deployment (e.g., Pixel, Chrome).
Dense: A powerful 31B parameter dense model that bridges the gap between server-grade performance and local execution.
Mixture-of-Experts: A highly efficient 26B MoE model designed for high-throughput, advanced reasoning.
You can download Gemma 4 models from Kaggle and Hugging Face. For more technical details on Gemma 4, see the Model Card. Earlier versions of Gemma core models are also available for download. For more information, see Previous Gemma models.

link for gemma 4 model info [https://ai.google.dev/gemma/docs/core]

**Direct Preference Optimization (DPO):** Training a model using preference data. For a single prompt, you provide a "chosen" (good) response and a "rejected" (bad) response. The model learns to increase the probability of the chosen response and decrease the probability of the rejected one. This directly targets negative constraints, teaching the model exactly what to avoid.

## Implimentation plan made with colaberation of Gemini AI:
Step 1: Dataset Construction

Use the Google AI Studio web interface to prompt Gemini to generate the prompt, chosen, and rejected JSONL triplets.

Commit the JSONL dataset to a GitHub repository via the GitHub web interface.

Step 2: Environment Setup

Create a Google Colab notebook and select a GPU hardware accelerator.

Execute !git clone [repository_url] in a cell to import the dataset.

Execute !pip install trl peft bitsandbytes transformers accelerate to install infrastructure libraries.

Step 3 & 4: SFT and DPO Execution

Write the training scripts within Colab cells.

Authenticate with Hugging Face using from huggingface_hub import notebook_login.

Execute the SFT and DPO training processes in the cloud GPU environment.

Push the trained LoRA adapter weights directly to the Hugging Face Hub using model.push_to_hub().

Step 5: Evaluation

Create a separate inference notebook in Colab.

Load the base Gemma model and merge the DPO adapters from Hugging Face.

Execute the evaluation prompts.
