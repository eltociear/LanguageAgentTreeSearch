# Official Repo of Language Agent Tree Search (LATS)

<p>
    <a href="https://www.python.org/">
        <img alt="Build" src="https://img.shields.io/badge/Python-3.7+-1f425f.svg?color=purple">
    </a>
    <a href="https://copyright.illinois.edu/">
        <img alt="License" src="https://img.shields.io/badge/License-MIT-blue">
    </a>
</p>

![teaser](pics/teaser.png)

Official implementation for paper [Language Agent Tree Search Unifies Reasoning Acting and Planing in Language Models]() with code, prompts, model outputs. 

More can be found at https://andyz245.github.io/LanguageAgentTreeSearch/

Check out our demo, CodeLATS at https://huggingface.co/spaces/AIatUIUC/CodeLATS/tree/main


### Reasoning + Acting (HotPotQA)

#### Setup

To get started:

1. Clone this repo and move to the HotPotQA directory:
```bash
git clone https://github.com/andyz245/LanguageAgentTreeSearch && cd LanguageAgentTreeSearch/hotpot
```

2. Install the module dependencies into your environment:
```bash
pip install -r requirements.txt
```

3. Set `OPENAI_API_KEY` environment variable to your OpenAI API key:
```bash
export OPENAI_API_KEY=<your key>
```

4. Set the scripts and run paper experiments
```bash
sh lats.sh
```

- ``--n_generate_sample``: number of times to prompt during expansion/sampling
- ``--n_evaluate_sample``: number of times to prompt for state evaluation
- ``--iterations``: maximum number of trajectories to sample

### Reasoning (Programming)

#### Setup

To get started:

1. Clone this repo and move to the HotPotQA directory:
```bash
git clone https://github.com/andyz245/LanguageAgentTreeSearch && cd LanguageAgentTreeSearch/programming
```

2. Install the module dependencies into your environment:
```bash
pip install -r requirements.txt
```

3. Set `OPENAI_API_KEY` environment variable to your OpenAI API key:
```bash
export OPENAI_API_KEY=<your key>
```

4. Set the scripts and run paper experiments
```bash
sh run_lats.sh
```

Code adapted from https://github.com/noahshinn024/reflexion/tree/main

### Decision-making (WebShop)

#### Setup

To get started:

1. Clone this repo and move to the WebShop directory:
```bash
git clone https://github.com/andyz245/LanguageAgentTreeSearch && cd LanguageAgentTreeSearch/webshop
```

2. Install WebShop from source and run environment instance locally. (https://github.com/princeton-nlp/WebShop)

3. Install the module dependencies into your environment:
```bash
pip install -r requirements.txt
```

4. Set `OPENAI_API_KEY` environment variable to your OpenAI API key:
```bash
export OPENAI_API_KEY=<your key>
```

5. Change localhost in lats.py to your port running WebShop

6. Set the scripts and run paper experiments
```bash
sh lats.sh
```

- ``--n_generate_sample``: number of times to prompt during expansion/sampling
- ``--n_evaluate_sample``: number of times to prompt for state evaluation
- ``--iterations``: maximum number of trajectories to sample

## Trajectories
``programming/root/`` contains all the trajectories from the paper's experiments on programming. Please use get_acc.py with the log path to get the actual accuracy. HotPotQA and WebShop logs were too large to upload, feel free to email if interested.

## Citations
Please cite the paper and star this repo if you use LATS and find it interesting/useful, thanks! Feel free to contact andyz3@illinois.edu or open an issue if you have any questions.

```bibtex
@misc{zhou2023language,
      title={Language Agent Tree Search Unifies Reasoning Acting and Planning in Language Models}, 
      author={Andy Zhou and Kai Yan and Michal Shlapentokh-Rothman and Haohan Wang and Yu-Xiong Wang},
      year={2023},
      eprint={2310.04406},
      archivePrefix={arXiv},
      primaryClass={cs.AI}
}

```
