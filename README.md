# Jigsaw Puzzles: Splitting Harmful Questions to Jailbreak Large Language Models
The repo is for paper [Jigsaw Puzzles: Splitting Harmful Questions to Jailbreak Large Language Models](https://arxiv.org/abs/2410.11459).
## Reproducibility
For safety and ethics concerns, we do not publicly release the complete jailbreak code, but we provide enough details for reproducibility. The data and code access will be granted via submitting a form indicating the researchers’ affiliation and the intention of use.
## Jigsaw Puzzles (JSP) Jailbreak
### Multi-turn Interactions
The JSP strategy leverages the multi-turn interaction capability of LLMs to perform jailbreaking. The jailbreaking process starts by inputting JSP prompt into the LLM, and then the split fractions of the harmful question are sequentially fed into the model as inputs in each turn. Once LLMs receive all the fractions, inputting “Begin” triggers LLMs to generate responses.


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/process.png" width="50%">
</div>

### JSP Prompt
JSP prompt is built upon two strategies essential for successful jailbreaking: Prohibition of Concatenated Question Generation and Inclusion of a Disclaimer. This dual approach enables JSP to effectively bypass the safeguards of LLMs, and induce responses to harmful queries.


<div align="center">
<img src="https://github.com/YangHao97/JigSawPuzzles/blob/main/resources/prompt.png" width="80%">
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
