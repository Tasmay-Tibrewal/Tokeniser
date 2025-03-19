---
license: mit
language:
- en
tags:
- tokeniser
pretty_name: tokeniser on val, test set of Slim Pajama
size_categories:
- 1B<n<10B
---

# Tokenizer

This is a tokeniser created on a custom-written algorithm on a huge vocabulary of `~1B` tokens. These tokens are given in the files (such that they are `<2GB` each, making them trackable by Git LFS). The text corpus is from the `SlimPajama` dataset by cerebras and consists of the whole text and validation corpus.
The final tokeniser is available in two versions (`0.5B` version - Val. data only and `1B` version - Val data + Test data, created using the same algo).
The files includes the token counts, the text corpus used, individual lines/paras from SlimPajama as a list JSON, ordered tokeniser with token ids (in order of their counts), unordered tokeniser  with token ids.

The tokeniser contains 131,072 tokens. 

## To do:
- Write custom code for the final tokenisation part (to break text into tokens)
- Create a python library for using the tokeniser
- Put the files on GitHub for a general overview
- Release the experimentation notebook and the tokenisation code (as part of the library)
- Make a writeup to explain the algo used

`Note: algo used is no industry standard algo like Byte Pair encoding, infact i have not studied BPE yet, i wanted to create a tokeniser from scratch first without any idea of what is currently used, and then compare the two, so a lot of what i implement may have similarities to that in industry but may not provide some performance improvement`

I am storing it on HF, not on GITHUB, because of storage issues, and due to easy availability for the AI community.