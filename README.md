# 🤗 Intro to Hugging Face Transformers — ACM-W Workshop

A hands-on, beginner-friendly workshop on using (and fine-tuning!) transformer models with the Hugging Face ecosystem — built for ACM-W.


[![Open Starter in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1pqa7Vt1NHxxd3AtOKhA_Nt3EcJaB3_Qp?usp=sharing)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

No prior machine learning experience required. If you can run a code cell, you can do this.

---

## About

This repo contains the materials for a hands-on workshop introducing [Hugging Face Transformers](https://huggingface.co/docs/transformers/index). Attendees go from "what even is a transformer?" to fine-tuning and deploying their own model, all inside a free Google Colab notebook — no local setup needed.

## What you'll learn

- What transformer models are, conceptually
- Using the `pipeline()` API for sentiment analysis, text generation, summarization, zero-shot classification, translation, named entity recognition, question answering, and fill-mask
- What's happening under the hood: tokenizers and models
- Browsing and swapping models on the Hugging Face Hub
- Loading real datasets with the `datasets` library
- **Fine-tuning your own model** on real data, with before/after evaluation
- Deploying a model as a shareable web app with **Gradio**

## Repo contents

| File | Description |
|---|---|
| [`notebooks/workshop_solution.ipynb`](notebooks/workshop_solution.ipynb) | The complete, fully-working notebook. Use this as the facilitator's reference, or for self-paced learners who want everything filled in. |
| [`notebooks/workshop_starter.ipynb`](notebooks/workshop_starter.ipynb) | **The code-along version for attendees.** All explanations are intact, but key lines are left as `TODO`s to fill in live during the workshop. |
| [`resources/CHEATSHEET.md`](resources/CHEATSHEET.md) | A quick-reference of pipeline tasks and snippets to keep after the workshop ends. |

## Getting started

**If you're attending the workshop:** click the **"Open Starter in Colab"** badge above. That's it — no installs, no local setup.

### Prerequisites
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
