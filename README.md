## Medical AI Chatbot Using LLaMA 2 with PEFT, LoRA & QLoRA
# Project Overview

This project focuses on building a Medical AI Chatbot powered by LLaMA 2, a modern large language model capable of understanding and generating medically relevant responses. The system provides users with suggestions, precautions, and specialist recommendations based on symptom descriptions. To efficiently fine-tune the model on limited hardware, advanced Parameter-Efficient Fine-Tuning (PEFT) methods—LoRA and QLoRA—are used. These approaches significantly reduce training cost while maintaining high performance.

# Key Features

Generates medical recommendations, precautions, and specialist referrals from user-provided symptoms.

Effectively interprets medical terms, abbreviations, and symptom descriptions.

Optimized to run on resource-limited environments like Google Colab through PEFT-based fine-tuning.

# Dataset

Source: AI Medical Chatbot Dataset

Total Records: 228,722

Unique Patients: 246,006

Unique Doctors: 242,150

Main Fields: Description, Patient, Doctor

This dataset includes real-world medical descriptions that help train the model to understand a wide variety of symptoms and conditions.

# Model Architecture
Base Model

LLaMA 2 – chosen for its strong reasoning and text-generation capabilities.

Fine-Tuning Techniques

PEFT: Allows fine-tuning selected model components instead of the entire network.

LoRA: Uses low-rank matrices to reduce training memory requirements.

QLoRA: Combines quantization with LoRA to achieve maximum efficiency on smaller GPUs.

# Implementation Workflow

Environment Setup
Install core libraries such as transformers, peft, datasets, and bitsandbytes.

Dataset Processing
Clean, prepare, and tokenize medical symptom descriptions.

Fine-Tuning
Apply LoRA and QLoRA to adapt LLaMA 2 for medical-response generation.

Inference
Input medical symptoms and obtain model-generated recommendations.

Evaluation
Assess performance using accuracy scores and sample predictions.

# System Requirements
Hardware

Minimum: 8 GB RAM, GPU-enabled Google Colab environment

Recommended: 16 GB RAM for smoother training

Python Libraries

transformers

datasets

peft

bitsandbytes

torch

Install Dependencies:

pip install transformers datasets peft bitsandbytes torch

Usage Instructions

Clone the repository:

git clone https://github.com/Daniyal-DS/AI-Medical-Chatbot
cd Medical-AI-Chatbot


Open the notebook:

jupyter notebook Medical_Ai_Chatbot.ipynb


Upload the dataset and run the notebook cells in sequence for training, evaluation, and inference.

Results

Validation Accuracy: ~89%

Example:
Input: “Patient experiencing shortness of breath and chest pain.”
Output: “Recommended Specialist: Cardiologist. Precautions: Avoid physical exertion and seek immediate medical attention.”

Challenges & Solutions

Limited GPU Resources: LoRA and QLoRA significantly reduced memory usage, enabling training on smaller GPUs.

Understanding Medical Terminology: Domain-aware preprocessing and tokenization improved the model’s ability to interpret clinical descriptions.

Repository Structure

medical_ai_chatbot.ipynb – Full implementation notebook

dataset/ – Directory for dataset files

images/ – Plots, visualizations, and architecture diagrams

README.md – Main documentation

Future Enhancements

Convert the model into a web or mobile application with a user-friendly interface.

Expand dataset diversity to cover more diseases and medical conditions.

Integrate multilingual support for broader accessibility.
