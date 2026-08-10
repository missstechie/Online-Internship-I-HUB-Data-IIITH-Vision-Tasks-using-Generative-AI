Generative AI Learning Projects

A collection of hands-on Generative AI projects exploring local AI deployment, model workflows, prompt engineering, and domain-specific Large Language Model fine-tuning.

1. Local Generative AI with ComfyUI
Overview

This project explores local Generative AI using ComfyUI, an open-source node-based interface for building and executing Stable Diffusion workflows.

The project focuses on understanding local model execution, node-based AI pipelines, prompt engineering, and resource-aware image generation.

Workflow
                    Text Prompt
                         ↓
                 Prompt Encoding
                         ↓
              Latent Image Generation
                         ↓
                 Diffusion Sampling
                         ↓
                    VAE Decoding
                         ↓
                   Generated Image

Key Learning Outcomes

Local deployment of Generative AI models
Stable Diffusion workflow understanding
Prompt engineering fundamentals
Node-based workflow design
Resource-aware AI execution
Reproducible AI workflows


2. Indian Legal Question Answering using LoRA Fine-Tuning
   
Overview

This project explores domain-specific fine-tuning of a Large Language Model (LLM) for Indian legal question answering using Low-Rank Adaptation (LoRA).

The project uses Qwen2.5-7B as the base model and Indian Legal Data v2 as the domain-specific dataset. The model is loaded using 4-bit quantization and fine-tuned with LoRA adapters on a Google Colab NVIDIA Tesla T4 GPU.

The goal is to demonstrate how a general-purpose language model can be adapted to a specialized domain using parameter-efficient fine-tuning techniques.

Objectives

Understand domain-specific LLM fine-tuning
Learn the fundamentals of LoRA
Use 4-bit quantization for memory-efficient model loading
Prepare an Indian legal instruction-response dataset
Fine-tune Qwen2.5-7B using LoRA
Evaluate the resulting model on Indian legal questions
Compare the base model vs. fine-tuned model

Dataset

Indian Legal Data v2

Property	Details
Domain	Indian Legal Question Answering
Total Examples	171,640
Fields	instruction, response
Training Subset	5,000 examples

For the initial experiment, 5,000 examples were selected from the complete dataset to allow efficient training within the available Google Colab GPU resources.

Fine-Tuning Pipeline

             Indian Legal Dataset
                       ↓
                Data Preparation
                       ↓
                  Qwen2.5-7B
                       ↓
                4-bit Quantization
                       ↓
                  LoRA Adapters
                       ↓
                    Training
                       ↓
            Indian Legal Q&A Model
                       ↓
               Model Evaluation

Training Configuration

Parameter	Value
Base Model	Qwen2.5-7B
Fine-Tuning Method	LoRA
Quantization	4-bit
Training Examples	5,000
Training Steps	60
GPU	NVIDIA Tesla T4
Training Loss	1.0021
Peak GPU Memory	10.344 GB

Evaluation

The fine-tuned model was evaluated using Indian legal questions covering topics such as:

Article 21 of the Indian Constitution
Article 32 of the Indian Constitution
Judicial Review in India
Writ Petitions
Civil vs. Criminal Cases

A before-and-after comparison was performed using the same questions with:

Base Qwen2.5-7B → LoRA Fine-Tuned Qwen2.5-7B

This helped evaluate the effect of domain-specific fine-tuning on the model's legal responses.

Key Features

⚖️ Indian Legal Domain Specialization
💬 Legal Question Answering
🧠 Domain-Specific LLM Adaptation
🔧 Parameter-Efficient LoRA Fine-Tuning
💾 4-bit Memory-Efficient Model Loading
📚 Instruction-Response Based Training
🔄 Reusable LoRA Adapter
🖥️ Designed for Limited GPU Resources


Learning Outcomes

Through this project, the following concepts were explored:

Large Language Model fine-tuning
Parameter-efficient fine-tuning
LoRA and QLoRA concepts
4-bit model quantization
Instruction-response dataset preparation
Supervised fine-tuning
Model evaluation and comparison
GPU memory management
Domain-specific AI adaptation

Limitations

The model was trained using a relatively small subset of the available dataset and only 60 training steps for the initial experiment. Some generated responses also showed repetition.

The project is intended as an educational and research prototype and should not be used as a source of professional legal advice.

 Future Scope
 
ComfyUI

Image-to-image generation
ControlNet integration
Inpainting and outpainting
Video generation
Advanced workflow optimization.

Indian Legal LLM

Train using a larger portion of the dataset
Increase training steps and experiment with epochs
Improve response quality and reduce repetition
Build a dedicated legal Q&A interface
Explore Retrieval-Augmented Generation (RAG)
Evaluate using larger benchmark datasets
Experiment with different base models and LoRA configurations

👨‍💻 Author

Generative AI Learning Project

Exploring Generative AI through practical experimentation, model adaptation, and hands-on implementation.
