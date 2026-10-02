# 🤗 Intro to Hugging Face Transformers — ACM-W Workshop

A hands-on, beginner-friendly workshop on using (and fine-tuning!) transformer models with the Hugging Face ecosystem — built for ACM-W.

[![Open Starter in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1pqa7Vt1NHxxd3AtOKhA_Nt3EcJaB3_Qp?usp=sharing) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

No prior machine learning experience required. If you can run a code cell, you can do this.



## About

This repo contains the materials for a hands-on workshop introducing [Hugging Face Transformers](https://huggingface.co/docs/transformers/index). Attendees learn about fine-tuning and deploying their own model, all inside a free Google Colab notebook — no local setup needed.



## Learning Objectives

By the end of this workshop, participants will be able to:

1. Explain, at a conceptual level, how transformer models process text
2. Use the `pipeline()` API to perform sentiment analysis, text generation, summarization, zero-shot classification, translation, named entity recognition, question answering, and masked language modeling
3. Describe the role of tokenizers and models as components of a pipeline, and invoke them independently
4. Locate, evaluate, and select models from the Hugging Face Hub
5. Load and inspect datasets using the Hugging Face `datasets` library
6. Fine-tune a pre-trained model on a custom dataset and evaluate its performance before and after training
7. Deploy a trained model as a shareable web application using Gradio



## Repository Structure

```
acmw-transformers/
├── README.md
├── LICENSE
├── notebooks/
│   ├── workshop_solution.ipynb    Complete, fully-executable reference notebook
│   └── workshop_starter.ipynb     Guided notebook with select cells left as exercises
└── resources/
    └── CHEATSHEET.md              Quick-reference of pipeline tasks and code snippets
```

---
## Getting started

**If you're attending the workshop:** click the **"Open Starter in Colab"** badge above. That's it — no installs, no local setup.


#### Prerequisites
1. A Google account (for Colab)
2. Once the notebook opens: **File → Save a copy in Drive**, so your edits are saved
3. **Enable a free GPU:** Runtime → Change runtime type → **T4 GPU** (needed for the fine-tuning section to run quickly; most other sections work fine on CPU)



## Further resources

- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — free, goes deeper on everything covered here
- [Hugging Face Hub](https://huggingface.co/models) — browse models
- [Hugging Face Spaces](https://huggingface.co/spaces) — live ML demos
- [Datasets documentation](https://huggingface.co/docs/datasets)
- [Gradio documentation](https://www.gradio.app/docs)


## Feedback

Found an issue with the notebooks, or have suggestions? Open an issue in this repo, or reach out to the ACM-W chapter directly.



## License

This project is licensed under the [MIT License](LICENSE) — feel free to reuse and adapt these materials for your own chapter or workshop, with attribution appreciated.

---

*Built for and by ACM-W 💜*
