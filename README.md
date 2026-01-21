# Single-Hop Question Answering with Classical and Transformer-based Retrieval Models

This repository contains an end-to-end, reproducible single-hop question answering (QA) pipeline for benchmarking classical sparse retrievers and transformer-based retrieval and QA models under a unified evaluation framework.

The project studies how retrieval design choices and fine-tuning strategies affect sentence-level retrieval accuracy, end-to-end QA performance, and convergence behavior on SQuAD 2.0.

---

## 🔧 Features

- Unified evaluation framework for single-hop QA  
- Supports classical sparse retrievers (TF-IDF, BM25) and dense / transformer-based models  
- Fine-tuning and evaluation of multiple BERT-family QA models (BERT, ALBERT, RoBERTa)  
- Modular and reproducible training pipeline  
- Component-level ablation analysis for retrieval and fine-tuning design choices  
- Experiment tracking and visualization with Weights & Biases (wandb)  

---

## 📊 Key Results

- Fine-tuned BERT-family QA model improves sentence retrieval accuracy from **32.5% to 88.2%** (2.7× improvement)  
- Systematic ablation quantifies the impact of:
  - Retriever type (sparse vs. dense)
  - Fine-tuning vs. frozen encoders  
  - Retrieval–reader interaction  
- End-to-end inference time remains nearly constant while accuracy improves significantly  

---

## 🧠 Methods

The pipeline consists of three main components:

1. **Retriever**
   - TF-IDF  
   - BM25  
   - Sentence encoders (dense retrieval)

2. **Reader / QA Model**
   - BERT, ALBERT, RoBERTa
   - Fine-tuned transformer models on SQuAD 2.0  

3. **Evaluation**
   - Exact Match (EM)  
   - F1 score  
   - Sentence-level retrieval accuracy  
   - Convergence and stability analysis  

All components are evaluated under a unified and reproducible framework.
