# 🤗 Intro to Hugging Face Transformers — ACM-W Workshop

A hands-on, beginner-friendly workshop on using (and fine-tuning!) transformer models with the Hugging Face ecosystem — built for ACM-W.

> ⚠️ **Before pushing:** replace `YOUR-USERNAME/YOUR-REPO-NAME` in the badge links below with your actual GitHub path, or the "Open in Colab" buttons won't work.

[![Open Solution in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR-USERNAME/YOUR-REPO-NAME/blob/main/notebooks/workshop_solution.ipynb)
[![Open Starter in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR-USERNAME/YOUR-REPO-NAME/blob/main/notebooks/workshop_starter.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

No prior machine learning experience required. If you can run a code cell, you can do this.

---

## 📖 About

This repo contains the materials for a ~2 hour (trimmable to 90 min) hands-on workshop introducing [Hugging Face Transformers](https://huggingface.co/docs/transformers/index). Attendees go from "what even is a transformer?" to fine-tuning and deploying their own model, all inside a free Google Colab notebook — no local setup needed.

## 🎯 What you'll learn

- What transformer models are, conceptually
- Using the `pipeline()` API for sentiment analysis, text generation, summarization, zero-shot classification, translation, named entity recognition, question answering, and fill-mask
- What's happening under the hood: tokenizers and models
- Browsing and swapping models on the Hugging Face Hub
- Loading real datasets with the `datasets` library
- **Fine-tuning your own model** on real data, with before/after evaluation
- Deploying a model as a shareable web app with **Gradio**
- Why models can be biased, and how to think about responsible use

## 📂 Repo contents

| File | Description |
|---|---|
| [`notebooks/workshop_solution.ipynb`](notebooks/workshop_solution.ipynb) | The complete, fully-working notebook. Use this as the facilitator's reference, or for self-paced learners who want everything filled in. |
| [`notebooks/workshop_starter.ipynb`](notebooks/workshop_starter.ipynb) | **The code-along version for attendees.** All explanations are intact, but key lines are left as `TODO`s to fill in live during the workshop. |
| [`resources/CHEATSHEET.md`](resources/CHEATSHEET.md) | A quick-reference of pipeline tasks and snippets to keep after the workshop ends. |

## 🚀 Getting started

**If you're attending the workshop:** click the **"Open Starter in Colab"** badge above. That's it — no installs, no local setup.

**If you want to see the finished product first (or are facilitating):** click **"Open Solution in Colab"**.

### Prerequisites
1. A Google account (for Colab)
2. Once the notebook opens: **File → Save a copy in Drive**, so your edits are saved
3. **Enable a free GPU:** Runtime → Change runtime type → **T4 GPU** (needed for the fine-tuning section to run quickly; most other sections work fine on CPU)

## 🗓️ Agenda

| Time | Section |
|---|---|
| 0:00–0:08 | What is a Transformer? |
| 0:08–0:13 | Setup |
| 0:13–0:23 | Your first pipeline: sentiment analysis |
| 0:23–0:38 | Tour of pipelines (generation, summarization, zero-shot, translation, NER, QA, fill-mask) |
| 0:38–0:46 | Under the hood: tokenizers |
| 0:46–0:54 | Under the hood: models |
| 0:54–1:01 | Exploring the Hugging Face Hub |
| 1:01–1:06 | Meet the Datasets library |
| 1:06–1:21 | Fine-tuning your own model |
| 1:21–1:29 | Build a web demo with Gradio |
| 1:29–1:34 | Responsible use & bias |
| 1:34–1:44 | Bonus: beyond text (images, CLIP) |
| 1:44–1:54 | Mini challenge |
| 1:54–2:00 | Wrap-up & resources |

*(Running the 90-minute version? See the facilitator notes at the top of the solution notebook for what to trim.)*

## 🔗 Further resources

- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — free, goes deeper on everything covered here
- [Hugging Face Hub](https://huggingface.co/models) — browse models
- [Hugging Face Spaces](https://huggingface.co/spaces) — live ML demos
- [Datasets documentation](https://huggingface.co/docs/datasets)
- [Gradio documentation](https://www.gradio.app/docs)

## 💬 Feedback

Found an issue with the notebooks, or have suggestions? Open an issue in this repo, or reach out to the ACM-W chapter directly.

## 📜 License

This project is licensed under the [MIT License](LICENSE) — feel free to reuse and adapt these materials for your own chapter or workshop, with attribution appreciated.

---

*Built for and by ACM-W 💜*
