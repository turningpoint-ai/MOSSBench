# MOSSBench: Is Your Multimodal Language Model Oversensitive to Safe Queries? 

![Oversensitive](https://img.shields.io/badge/Task-Oversensitive-red) 
![Safety Alignment](https://img.shields.io/badge/Task-Safety_Alignment-red) 
![Multi-Modal](https://img.shields.io/badge/Task-Multi--Modal-red) 
![MOSSBench](https://img.shields.io/badge/Dataset-MOSSBench-blue)  
![GPT-4](https://img.shields.io/badge/Model-GPT--4-green) 
![Gemini-Pro](https://img.shields.io/badge/Model-Gemini--Pro-green)
![Claude-3](https://img.shields.io/badge/Model-Claude--3-green)  

Code for the Paper "[MOSSBench: Is Your Multimodal Language Model Oversensitive to Safe Queries?](https://arxiv.org/abs/2406.17806)".

For more details, please refer to the project page with dataset exploration and visualization tools: [https://turningpoint-ai.github.io/MOSSBench/](https://turningpoint-ai.github.io/MOSSBench/).

:bell: If you have any questions or suggestions, please don't hesitate to let us know. You can comment on the [Twitter](https://x.com/TurningPointAI/status/1807169697571553574), or post an issue on this repository.

[[Webpage](https://turningpoint-ai.github.io/MOSSBench/)] [[Paper](https://arxiv.org/abs/2406.17806)] [[Huggingface Dataset](https://huggingface.co/datasets/AIcell/MOSSBench)] [[Visualization](https://turningpoint-ai.github.io/MOSSBench/#visualization)] [[Result Explorer](https://turningpoint-ai.github.io/MOSSBench/#explorer)] [[Twitter](https://x.com/TurningPointAI/status/1807169697571553574)]

<p align="center">
    <img src="website\static\images\psych.webp" width="40%"> <br>
   Logo for <b>MOSSBench</b> generated by DALL·E 3.
</p>

## Outlines

- [💥 News 💥](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#-news-)
- [👀 About MOSSBench](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#-about-mossbench)
- [🏆 Leaderboard 🏆](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#-leaderboard-)
  - [Contributing the Leaderboard](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#contributing-the-leaderboard)
- [📊 Dataset Examples](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#-dataset-examples)
- [📖 Dataset Usage](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#-dataset-usage)
  - [Data Downloading](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#data-downloading)
  - [Data Format](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#data-format)
  - [Data Visualization](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#data-visualization)
  - [Usage Demos](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#usage-demos)
- [🔮 Evaluations on MOSSBench](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#-evaluations-on-mathvista)
  - [Requirements (Optional)](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#requirements-optional)
  - [Downloading Images (Optional)](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#downloading-images-optional)
  - [Evaluation Pipelines](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#evaluation-pipelines)
- [📜 License](https://github.com/turningpoint-ai/MOSSBench/README.md#-license)
- [☕ Stay Connected!](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#coffee-stay-connected)
- [✅ Cite](https://github.com/turningpoint-ai/MOSSBench/blob/main/README.md#white_check_mark-cite)



## 💥 News 💥
<!-- - **[2024.06.22]** 💥 **Claude 3.5 Sonnet achieves new SOTA** on MathVista with **67.7**! Learn more at the [Anthropic blog](https://www.anthropic.com/news/claude-3-5-sonnet). -->
<!-- - **[2024.05.13]** 💥 **OpenAI's GPT-4o Outperforms Humans on MathVista!** For the first time, OpenAI's new GPT-4o model has achieved a higher score than the human average on MathVista, scoring **63.8** compared to humans' **60.3**. Learn more at the [OpenAI blog](https://openai.com/index/hello-gpt-4o/).
- **[2024.01.16]** 🌟 Our **MathVista** paper has been accepted for an **Oral** presentation at **ICLR 2024** (only top 85 out of over 7200 submissions)! 🎉 Cheers!
- **[2023.12.21]** 🚀 [Qwen-VL-Plus](https://github.com/QwenLM/Qwen-VL) achieves **43.3%**, establishing itself as the best-performing one in open-sourced models. 🎉 Congratulations!
- **[2023.12.08]** 🔍 We've updated the leaderboard and radar graphs with the **fine-grained scores** of the **Gemini** family models. Thanks to the Gemini Team and Google for providing us with these results! 👏
- **[2023.12.06]** 🚀 Google's newly released multimodal model, [Gemini](https://blog.google/technology/ai/google-gemini-ai/), shows impressive abilities on **MathVista**, achieving a new SOTA performance with **50.3%**! 🎉  Cheers!!
- **[2023.11.17]** 🌟 Congratulations to [SPHINX (V2)](https://github.com/Alpha-VLLM/LLaMA2-Accessory/tree/main/SPHINX), which is now the SOTA open-source multimodal model on **MathVista**, reaching **36.7%**. 👏
- **[2023.10.25]** 🚀 Dive into our comprehensive **112-page** evaluation of **GPT-4V**, Bard, and other Large Multimodal Models, encompassing both **quantitative** and **qualitative** insights. [Explore the full paper now!](https://arxiv.org/abs/2310.02255) 📄✨
- **[2023.10.16]** 🔍 We are working on a comparative study on the **GPT-4V** model. Stay tuned for the detailed report! 📑.
- **[2023.10.15]** We finished the manual evaluation of **GPT-4V** with the playground chatbot on the *testmini* set on **MathVista**. 🚀 GPT-4V achieves a substantial gain of **15.1%** ⬆️ over Bard, reaching a new record of **49.9%**! 🎉
- **[2023.10.15]** Our dataset is now accessible at [Huggingface Datasets](https://huggingface.co/datasets/AI4Math/MathVista).
- **[2023.10.15]** Our dataset is now accessible at [Paper With Code](https://paperswithcode.com/dataset/mathvista).
- **[2023.10.03]** The top-performing model, 🎭 **Multimodal Bard**, achieved a score of **34.8%** on the *testmini* set for **MathVista** 📊.
- **[2023.10.03]** Our work was featured by [Aran Komatsuzaki](https://twitter.com/arankomatsuzaki) on [Twitter](https://twitter.com/arankomatsuzaki/status/1709380140717809992). Thanks! -->
- **[2024.06.22]** Our paper is now accessible at [ArXiv](https://arxiv.org/abs/2406.17806).

## 👀 About MOSSBench

Humans are prone to **cognitive distortions** — biased thinking patterns that lead to exaggerated responses to specific stimuli, albeit in very different contexts. This paper demonstrates that advanced MLLMs exhibit similar tendencies. While these models are designed to respond queries under safety mechanism, they sometimes **reject harmless queries** in the presence of certain visual stimuli, disregarding the benign nature of their contexts.

<p align="center">
    <img src="website/static/images/main_plot.png" width="70%"> <br>
  Overview of <b>MOSSBench</b>. MLLMs exhibit behaviors similar to human cognitive distortions, leading to oversensitive responses where benign queries are perceived as harmful. We discover that oversensitivity prevails among existing MLLMs.
</p>

As the initial step in investigating this behavior, we identify **three types of stimulus** that trigger the oversensitivity of existing MLLMs: **Exaggerated Risk**, **Negated Harm**, and **Counterintuitive Interpretation**. To systematically evaluate MLLMs' oversensitivity to these stimuli, we propose the Multimodal OverSenSitivity Benchmark Logo (MOSSBench). This toolkit consists of 300 manually collected benign multimodal queries, cross-verified by third-party reviewers (AMT).

<p align="center">
    <img src="website/static/images/stimuli.jpg" width="70%"> <br>
    Three types of stimuli in <b>MOSSBench</b>.
</p>

Empirical studies using Logo MOSSBench on 20 MLLMs reveal several insights: (1). Oversensitivity is **prevalent** among SOTA MLLMs, with refusal rates reaching up to 76% for harmless queries. (2). **Safer models** are **more oversensitive**: increasing safety may inadvertently raise caution and conservatism in the model's responses. (3). **Different types of stimuli** tend to cause errors at **specific stages** — perception, intent reasoning, and safety decision-making — in the response process of MLLMs. These findings highlight the need for refined safety mechanisms that balance caution with contextually appropriate responses, improving the reliability of MLLMs in real-world applications.

For more details, you can find our project page [here](https://turningpoint-ai.github.io/MOSSBench/) and our paper [here](https://arxiv.org/abs/2406.17806).

## 🏆 Leaderboard 🏆

### Contributing the Leaderboard

🚨🚨 The leaderboard is continuously being updated. 

The evaluation instructions are available at [🔮 Evaluations on MOSSBench](https://github.com/turningpoint-ai/MOSSBench?tab=readme-ov-file#-evaluations-on-mossbench) and [📝 Evaluation Scripts of Our Models](https://github.com/turningpoint-ai/MOSSBench?tab=readme-ov-file#-evaluation-scripts-of-our-models).

To submit your results to the leaderboard, please send to [this email](mailto:xiruili@g.ucla.edu) with your result file (**we will generate the score file for you**), referring to the template file below:

- [output_test_template_for_leaderboard_submission.json](https://github.com/turningpoint-ai/MOSSBench/blob/main/results/submission_template.json)

### Oversensitivity on MOSSBench

**Refusal Rate** of mllms:

| **#** | **Model**           |                                  **Availability**                              | **Date**   | **ALL**  | **Exaggerated Risk** | **Negated Harm** | **Counterintuitive Interpretation** |
| ----- | ------------------------------------ | ------------------------------------------------------------ | ---------- | -------- | ------- | ------- | ------- |
| 1     | **Claude 3 Opus (web)**                        | Proprietary MLLMs - Web version                     | 2024-06-22 | **70.67** | 41    | 93    | 78   |
| 2     | **Gemini Advanced**                        | Proprietary MLLMs - Web version                     | 2024-06-22 | **61** | 41    | 67    | 75   |
| 3     | **Claude 3 Sonnet**                        | Proprietary MLLMs                   | 2024-06-22 | **55** | 39    | 65    | 61   |
| 4     | **Claude 3 Haiku**                        | Proprietary MLLMs                   | 2024-06-22 | **49.33** | 27    | 58    | 63   |
| 5     | **Claude 3 Opus**                        | Proprietary MLLMs                   | 2024-06-22 | **34.67** | 11    | 43    | 55   |
| 6     | **Gemini Pro 1.5**                        | Proprietary MLLMs                   | 2024-06-22 | **29.33** | 25    | 28    | 35   |
| 7     | **Qwen-VL-Chat**                        | Open-source MLLMs                   | 2024-06-22 | **21.67** | 16    | 13    | 36   |
| 8     | **InternLM-Xcomposer2-7b**                        | Open-source MLLMs                   | 2024-06-22 | **17.67** | 14    | 11    | 28   |
| 9     | **Gemini Pro Vision**                        | Proprietary MLLMs                   | 2024-06-22 | **17** | 20    | 9    | 22   |
| 10     | **Reka**                        | Proprietary MLLMs                   | 2024-06-22 | **16.67** | 11    | 21    | 18   |
| 11     | **InstructBLIP-Vicuna-7b**                        | Open-source MLLMs                   | 2024-06-22 | **15.67** | 21    | 23    | 3    |
| 12     | **IDEFICS-9b-Instruct**                        | Open-source MLLMs                   | 2024-06-22 | **13.67** | 17    | 9    | 15    |
| 13     | **MiniCPM-V 2.0**                        | Open-source MLLMs                   | 2024-06-22 | **12.33** | 16    | 11    | 10    |
| 14     | **LlaVA-1.5-7b**                        | Open-source MLLMs                   | 2024-06-22 | **12.33** | 18    | 10    | 9    |
| 15     | **mPLUG-Owl2**                        | Open-source MLLMs                   | 2024-06-22 | **10** | 11    | 7    | 12    |
| 16     | **LlaVA-1.5-13b**                        | Open-source MLLMs                   | 2024-06-22 | **9.67** | 9    | 9    | 11    |
| 17     | **GPT-4o**                        | Proprietary MLLMs                   | 2024-06-22 | **6.33** | 6    | 8    | 5    |
| 18     | **MiniCPM-Llama3-V 2.5**                        | Open-source MLLMs                   | 2024-06-22 | **6** | 8    | 5    | 5    |
| 19     | **GPT-4o**                        | Proprietary MLLMs - Web version                   | 2024-06-22 | **4** | 6    | 2    | 4    |

🔔 The automatic evaluation on [CodaLab](https://codalab.org/) are under construction. 


## 📊 Dataset Examples

Examples of 3 types of **oversensitivity stimuli**:

1. Exaggerated Risk

<img src="website/static/images/results-examples/Exaggerated.png" style="zoom:20%;" />

2. Negated Harm

<img src="website/static/images/results-examples/Negated.png" style="zoom:20%;" />

3. Counterintuitive Interpretation

<img src="website/static/images/results-examples/Counterintuitive.png" style="zoom:20%;" />


## 📖 Dataset Usage

### Data Downloading

You can download this dataset by the following command (make sure that you have installed [Huggingface Datasets](https://huggingface.co/docs/datasets/quickstart)):

```python
from datasets import load_dataset

dataset = load_dataset("AIcell/MOSSBench", "oversensitivity")
```

Here are some examples of how to access the downloaded dataset:

```python
# print the first example on the testmini set
print(dataset["train"][0])
print(dataset["train"][0]['pid']) # print the problem id 
print(dataset["train"][0]['question']) # print the question text 
print(dataset["train"][0]['image']) # print the image path
dataset["train"][0]['decoded_image'] # display the image
```

### Data Format

The dataset is provided in json format and contains the following attributes:

```
{
    "image": [string] A file path pointing to the associated image,
    "short description": [string] An oracle short description of the associated image,
    "question": [string] A query regarding to the image, 
    "pid": [string] Problem ID, e.g., "1",
    "metadata": {
        "over": [string] Oversensitivity type,
        "human": [integer] Whether image contains human, e.g. 0 or 1,
        "child": [integer] Whether image contains child, e.g. 0 or 1,
        "syn": [integer] Whether image is synthesized, e.g. 0 or 1,
        "ocr": [integer] Whether image contains ocr, e.g. 0 or 1,
        "harm": [integer] Which harm type the query belongs to, 0-7,
    }
}
```

### Data Visualization

🎰 You can explore the dataset in an interactive way [here](https://turningpoint-ai.github.io/MOSSBench/#visualization).

## 🔮 Evaluations on MOSSBench

### Requirements

Install the Python dependencies if you would like to reproduce our results for ChatGPT, GPT-4, Claude-2, and Bard:

```sh
pip install -r requirements.txt
```

### Downloading Images (Optional)

We provide images in the JPG format. You can download and unzip them using the following commands:

```sh
cd data
wget https://huggingface.co/datasets/AIcell/MOSSBench/resolve/main/images.zip
unzip images.zip && rm images.zip
```

This step might be optional if you prefer to use the Hugging Face format of the data.

### Evaluation Pipelines

#### Step 1. Prepare your MLLM

##### For proprietary MLLMs
Get your models API ready in following links 

- [OpenAI API key](https://platform.openai.com/account/api-keys)
- [Claude API Key](https://docs.anthropic.com/claude/reference/getting-started-with-the-api)
- [Gemini API Key](https://ai.google.dev/gemini-api/docs/api-key)

and store them under foler ```path_to_your_code/api_keys/[model].text```. Please replace the ```[model]``` by  ```anthropic_keys```, ```google_keys``` 
and ```openai_keys```.

##### For open-source MLLMs
Download your model or get their names for Huggingface. And replace the following path by where you locate your models or your models name.

```sh

# Initialize variables
MODEL_NAME="your_path_to/idefics-9b-instruct" # you can replace it by direct naming
DATA_DIR=""
```


**Step 2. Run evaluation** ([main.py](https://github.com/turningpoint-ai/MOSSBench/blob/experiments/main.py))
Next, run ```experiments/main.py``` file in folder or excute the ```.sh``` files we provide for evaluation by 


```sh
cd experiments/scripts

bash run_instructblip.sh
```

## 📜 License

The new contributions to our dataset are distributed under the [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license, including

- The creation of three dataset: IQTest, FunctionQA, and Paper;
- The filtering and cleaning of source datasets;
- The standard formalization of instances for evaluation purposes;
- The annotations of metadata.

- **Purpose:** The dataset was primarily designed for use as a test set.
- **Commercial Use:** The dataset can be used commercially as a test set, but using it as a training set is prohibited. By accessing or using this dataset, you acknowledge and agree to abide by these terms in conjunction with the [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.

## :coffee: Stay Connected!

Fantastic! We are always open to engaging discussions, collaborations, or even just sharing a virtual coffee. To get in touch or join our team, visit [TurningPoint AI](https://www.turningpoint-ai.com/)'s homepage for contact information.


## :white_check_mark: Cite

If you find **MOSSBench** useful for your your research and applications, please kindly cite using this BibTeX:

```latex
@misc{li2024mossbenchmultimodallanguagemodel,
      title={MOSSBench: Is Your Multimodal Language Model Oversensitive to Safe Queries?}, 
      author={Xirui Li and Hengguang Zhou and Ruochen Wang and Tianyi Zhou and Minhao Cheng and Cho-Jui Hsieh},
      year={2024},
      eprint={2406.17806},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2406.17806}, 
}
```

## MOSSBench Website

MOSSBench website is adapted from [Nerfies website](https://nerfies.github.io) and [MathVista website](https://mathvista.github.io/).

## Website License
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
