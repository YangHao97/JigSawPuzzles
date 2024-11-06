# Jigsaw Puzzles: Splitting Harmful Questions to Jailbreak Large Language Models
The repo is for paper [Jigsaw Puzzles: Splitting Harmful Questions to Jailbreak Large Language Models](https://arxiv.org/abs/2410.11459).
## Reproducibility
For safety and ethics concerns, we do not publicly release the complete jailbreak code, but we provide enough details for reproducibility. The data and code access will be granted via submitting a form indicating the researchers’ affiliation and the intention of use. [Access Form](https://docs.google.com/forms/d/e/1FAIpQLSfJM70VplmggxS52GHGG5D5nK-n3mwXnDUUACVFbShFFLlimw/viewform?usp=sf_link)
## Jigsaw Puzzles (JSP) Jailbreak
### Multi-turn Interactions
The JSP strategy leverages the multi-turn interaction capability of LLMs to perform jailbreaking. The jailbreaking process starts by inputting JSP prompt into the LLM, and then the split fractions of the harmful question are sequentially fed into the model as inputs in each turn. Once LLMs receive all the fractions, inputting “Begin” triggers LLMs to generate responses.


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/process.png" width="50%">
</div>

### JSP Prompt
JSP prompt is built upon two strategies essential for successful jailbreaking: **Prohibition of Concatenated Question Generation** and **Inclusion of a Disclaimer**. This dual approach enables JSP to effectively bypass the safeguards of LLMs, and induce responses to harmful queries.


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/prompt.png" width="80%">
</div>

### Splitting Strategy
We identify and isolate harmful words from their original queries, resulting in fragmented queries. The isolated harmful words are then further divided into meaningless and benign letter fractions. Our process is summarised in 3 stages: **Re-write Queries**, **Sentence-level Splitting**, **Word-level Splitting**.


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/splitting.png" width="80%">
</div>

### Jailbreak Performance


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/results.png" width="80%">
</div>

## Benchmark
We follow the settings of [Zeng et al.](https://arxiv.org/abs/2401.06373) to benchmark JSP jailbreaking with/without defence mechanisms against previous jailbreaking strategies.


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/benchmark.png" width="45%">
</div>

## Citation
```
@article{yang2024jigsaw,
  title={Jigsaw Puzzles: Splitting Harmful Questions to Jailbreak Large Language Models},
  author={Yang, Hao and Qu, Lizhen and Shareghi, Ehsan and Haffari, Gholamreza},
  journal={arXiv preprint arXiv:2410.11459},
  year={2024}
}
```
