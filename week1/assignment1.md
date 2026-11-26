# Assignment 1 — Information is surprise

**Due:** Sunday night, end of Week 1 · **Weight:** 15% of the project

## Tasks

1. **Entropy** (Parts 1–2 of `starter.ipynb`): implement `surprise`, `char_probs` and `entropy`. All tests must pass.
2. **Baselines** (Part 3): run the gzip / bzip2 / xz table. Add at least one text of your own: Hindi or Marathi in `data/indic.txt`, or anything else interesting (song lyrics you wrote, a chat export, DNA, a log file).
3. **Shannon game** (Part 4): play with at least one friend on 60+ characters. Record their average guesses and estimated bits/char.
4. **Huffman** (Part 5): implement `huffman_codes`, `encode` and `decode`. The round trip must be bit-exact and all tests must pass.
5. **Write-up** (Part 6): the comparison table plus answers to the four questions, in your repo's README.

## Submit

Push to your own GitHub repo:
- `week1/starter.ipynb`, run top to bottom **with outputs saved**
- `README.md` with the table and your answers

Then post your repo link in the group channel.

## How it's judged

| Criterion | Weight |
| --- | --- |
| All tests pass; Huffman round trip is bit-exact | 50% |
| Comparison table includes your own extra text | 20% |
| Written answers show you understand *why* (not just *what*) | 30% |

Bonus (no marks, just glory): whoever finds the text with the lowest gzip bpc that is still meaningful (not just `aaaa…`) gets a shout-out in the Week 2 session.
