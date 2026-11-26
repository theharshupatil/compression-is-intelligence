# Compression Is Intelligence

**Build a language model that beats gzip.** A 4-week guided project for WiDS 6.0, Analytics Club, IIT Bombay.

Every time you zip a file, you are making a prediction. Claude Shannon showed that a model which predicts the next symbol with probability *p* can store it in about −log₂ *p* bits. So **better prediction = smaller files**, and the cross-entropy loss every ML model minimises is literally a compressed size.

In this project you build a lossless compressor from scratch and keep upgrading its brain: from counting letters, to n-gram context models, to a small neural network and a tiny Transformer. Every improvement in prediction shows up as a smaller file. The scoreboard is one number: **bits per character (bpc)**.

## The scoreboard

Measured in `week1/starter.ipynb` on the first 200,000 characters of Tiny Shakespeare:

| Compressor | bits / char |
| --- | --- |
| Raw text (8-bit bytes) | 8.00 |
| Order-0 entropy (letters counted independently) | 4.76 |
| gzip (zlib, level 9) | 3.16 |
| xz (lzma, preset 9) | 2.85 |
| bzip2 (level 9) | 2.50 |
| **Your compressor (Week 4)** | **?** |

## Roadmap

| Week | Theme | You build |
| --- | --- | --- |
| 1 | Information is surprise | Entropy calculator, gzip/bzip2/xz baselines, Huffman coder |
| 2 | From probabilities to bits | Arithmetic coder + adaptive n-gram models → **zip v1** (midterm checkpoint) |
| 3 | Learning to predict | Char-level MLP and tiny Transformer plugged into your coder |
| 4 | llzip | Your neural compressor on the leaderboard + one extension of your choice |

Week 4 extensions: an online compressor that learns while it compresses, which language is most predictable (English vs Hindi vs Marathi vs code), gzip as a text classifier, compressing with pretrained GPT-2, an AI-text detector based on surprise, or compressing images and audio.

## Getting started

```bash
git clone https://github.com/theharshupatil/compression-is-intelligence.git
cd compression-is-intelligence
pip install jupyter
jupyter notebook week1/starter.ipynb
```

Week 1 needs only the Python standard library. Weeks 3–4 use PyTorch; Google Colab's free GPU is enough.

## Repository layout

```
week1/
  starter.ipynb     # fill in the TODOs; tests included
  assignment1.md    # what to submit
  resources.md      # what to read / watch
week2/ ... week4/   # released weekly
```

## Prerequisites

Comfortable with Python (functions, classes, lists and dicts) and basic NumPy. High-school probability and logarithms. No prior ML experience needed.

## Mentor

Harshvardhan Patil, Electrical Engineering, IIT Bombay.
