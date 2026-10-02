# 🤗 Hugging Face Transformers — Quick Reference

A cheat sheet of everything covered in the workshop. Keep this handy after the session!

## Install

```bash
pip install transformers datasets accelerate gradio torch
```

## The `pipeline()` pattern

Every pipeline follows the same shape:

```python
from transformers import pipeline

my_pipeline = pipeline("task-name")       # or pipeline("task-name", model="model/name")
result = my_pipeline("your input here")
```

## Common tasks

| Task | Pipeline name | Example call |
|---|---|---|
| Sentiment analysis | `sentiment-analysis` | `classifier("I love this!")` |
| Text generation | `text-generation` | `generator("Once upon a time", max_length=40)` |
| Summarization | `summarization` | `summarizer(long_text, max_length=60, min_length=20)` |
| Zero-shot classification | `zero-shot-classification` | `zero_shot(text, candidate_labels=["a", "b"])` |
| Translation | `translation_en_to_fr` (or other pairs) | `translator(text)` |
| Named entity recognition | `ner` | `ner(text, grouped_entities=True)` |
| Question answering | `question-answering` | `qa(question="...", context="...")` |
| Fill-mask | `fill-mask` | `unmasker("Paris is the <mask> of France.")` |
| Image classification | `image-classification` | `image_classifier(image_url)` |
| Zero-shot image classification | `zero-shot-image-classification` | `clip(image_url, candidate_labels=["a cat", "a dog"])` |

> 💡 Browse all task types at [huggingface.co/tasks](https://huggingface.co/tasks)

## Tokenizer & model, manually

```python
from transformers import AutoTokenizer, AutoModelForSequenceClassification
import torch
import torch.nn.functional as F

tokenizer = AutoTokenizer.from_pretrained("model-name")
model = AutoModelForSequenceClassification.from_pretrained("model-name")

inputs = tokenizer("some text", return_tensors="pt")
with torch.no_grad():
    outputs = model(**inputs)

probabilities = F.softmax(outputs.logits, dim=-1)
```

## Loading a dataset

```python
from datasets import load_dataset

dataset = load_dataset("dataset-name")
print(dataset)                 # see splits: train / validation / test
dataset["train"][0]            # look at one example
```

## Fine-tuning skeleton

```python
from transformers import AutoModelForSequenceClassification, TrainingArguments, Trainer
import numpy as np

def tokenize(batch):
    return tokenizer(batch["text"], truncation=True, padding="max_length", max_length=128)

tokenized = dataset.map(tokenize, batched=True)

model = AutoModelForSequenceClassification.from_pretrained("model-name", num_labels=2)

def compute_metrics(eval_pred):
    logits, labels = eval_pred
    predictions = np.argmax(logits, axis=-1)
    return {"accuracy": (predictions == labels).mean()}

training_args = TrainingArguments(
    output_dir="my-model",
    num_train_epochs=2,
    per_device_train_batch_size=16,
    eval_strategy="epoch",
)

trainer = Trainer(
    model=model,
    args=training_args,
    train_dataset=tokenized["train"],
    eval_dataset=tokenized["test"],
    compute_metrics=compute_metrics,
)

trainer.train()
trainer.evaluate()
```

## Deploying with Gradio

```python
import gradio as gr

def my_function(text):
    return my_pipeline(text)

demo = gr.Interface(fn=my_function, inputs="text", outputs="label")
demo.launch(share=True)   # share=True gives a public link (~72 hrs)
```

## Finding models on the Hub

1. Go to [huggingface.co/models](https://huggingface.co/models)
2. Filter by task in the sidebar
3. Sort by "Most downloads" or "Trending"
4. **Read the model card** — training data, limitations, intended use
5. Copy the model name into `pipeline("task", model="owner/model-name")`


---
*From the ACM-W Hugging Face Transformers Workshop*
