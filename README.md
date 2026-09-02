<div align="center">

```text
██████╗  █████╗ ███╗   ███╗██╗
██╔══██╗██╔══██╗████╗ ████║██║
██████╔╝███████║██╔████╔██║██║
██╔══██╗██╔══██║██║╚██╔╝██║██║
██║  ██║██║  ██║██║ ╚═╝ ██║██║
╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚═╝╚═╝
```

### AI / ML Engineer · Full-Stack Developer

[![Email](https://img.shields.io/badge/chamseddinerami@gmail.com-0a0a0a?style=for-the-badge&logo=gmail&logoColor=white)](mailto:chamseddinerami@gmail.com)
[![Zygoflow](https://img.shields.io/badge/zygoflow.com-f59e0b?style=for-the-badge)](https://zygoflow.com)

</div>

---

## About Me

I am a Computer Science graduate with a Master's degree in Computer Systems and Engineering, currently focusing on Machine Learning, AI, and full-stack development.

I enjoy building projects end-to-end: preparing data, training and evaluating models, building APIs, creating frontends, and deploying complete applications.

My current focus is on becoming an ML / AI Engineer and building practical projects that go beyond model training and include real deployment and engineering problems.

---

# Featured Projects

## Customer Support Intent Classifier

**Live Demo:**  
https://support-ticket-intent-classifier.vercel.app/

An end-to-end NLP project that classifies customer support messages into **27 intent categories**.

I built two different models and compared how well they generalize:

- Vanilla RNN implemented manually in PyTorch
- Fine-tuned DistilBERT Transformer

The RNN performed very well on a normal random test split, but I wanted to test whether it could generalize to more natural wording.

Because of that, I created a separate human-written challenge set with 81 examples.

### Results

| Model | Challenge Accuracy |
|---|---:|
| Vanilla RNN | 56.79% |
| DistilBERT | 90.12% |
| Quantized DistilBERT ONNX | 90.12% |

The pretrained Transformer generalized much better than the RNN.

### Deployment Optimization

The original DistilBERT model was too heavy for the available deployment memory.

Instead of increasing server resources, I optimized the inference pipeline:

```text
PyTorch DistilBERT
        ↓
ONNX export
        ↓
INT8 quantization
        ↓
256 MB → 64 MB
```

I also exported the RNN to ONNX, which allowed me to completely remove PyTorch from the production backend.

The final production backend uses:

```text
FastAPI
   ↓
ONNX Runtime
   ├── RNN ONNX
   └── DistilBERT INT8 ONNX
```

After quantization, DistilBERT kept the same:

```text
90.12% challenge accuracy
```

The application is deployed with:

- Next.js frontend on Vercel
- FastAPI backend on Render
- ONNX Runtime for inference

**Live Demo:**  
https://support-ticket-intent-classifier.vercel.app/

---

## Zygoflow

**Website:**  
https://zygoflow.com

Zygoflow is a web application I built for generating data-driven website components using natural language.

It combines AI-assisted website generation with database integration, so generated components can work with real application data instead of being only static UI.

**Tech:** Next.js · Firebase · Supabase · OpenAI API · Vercel

---

## Published Games

| Game | Platform |
|---|---|
| [World War 2: Defending Battle](https://play.google.com/store/apps/details?id=com.rsGaming.WorldWar2Defendingbattle) | Google Play |
| [Scream Hunter](https://play.google.com/store/apps/details?id=com.rsgaming.screamhunter) | Google Play |

---

# Technical Skills

### AI / Machine Learning

- Python
- PyTorch
- TensorFlow
- Hugging Face Transformers
- DistilBERT
- ONNX
- ONNX Runtime
- Model Quantization
- Scikit-learn
- NLP
- RNN / LSTM / GRU
- Transformers
- Embeddings
- Model Evaluation

### Backend

- FastAPI
- Django
- REST APIs
- Python
- Node.js

### Frontend

- React
- Next.js
- TypeScript
- JavaScript
- HTML / CSS
- Tailwind CSS

### Databases

- PostgreSQL
- Supabase
- Firebase
- SQLite

### DevOps / Deployment

- Docker
- Git
- GitHub
- Vercel
- Render
- DigitalOcean

### Languages

- Python
- JavaScript / TypeScript
- Java
- C#
- SQL

---

# What I Like Building

I am especially interested in projects where Machine Learning is part of a complete application rather than an isolated notebook.

For example:

```text
Data
↓
Training
↓
Evaluation
↓
Model optimization
↓
API
↓
Frontend
↓
Deployment
```

I want to understand and build the complete ML engineering workflow.

---

<div align="center">

### Contact

**Email:** chamseddinerami@gmail.com

**Customer Support Classifier:**  
https://support-ticket-intent-classifier.vercel.app/

**Zygoflow:**  
https://zygoflow.com

</div>
