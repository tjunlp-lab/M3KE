# M3KE


## Introduction

We propose **M3KE**, **a <u>M</u>assive <u>M</u>ulti-Level <u>M</u>ulti-Subject <u>K</u>nowledge <u>E</u>valuation benchmark**, which is developed to measure knowledge acquired by Chinese large language models in zero- and few-shot settings. We have collected 20,477 questions from 71 tasks. Our selection covers all major levels of Chinese education system, ranging from the primary school to college, as well as a wide variety of subjects, including humanities, history, politics, law, education, psychology, science, technology, art and religion. All questions are multiple-choice questions with four options, hence guaranteeing a standardized and unified assessment process.

We’ve assessed and will continue to assess a number of Chinese large language models on our benchmark. The currently assessed models are either only pre-trained on massive data or pre-trained + fine-tuned with SFT or RLHF. Model sizes vary from 335M to 175B parameters. 

This is collaborative research effort between the Natural Language Processing Laboratory at Tianjin University and Huawei Noah’s Ark Lab.

The comparison between M3KE and other relevant benchmarks.

| Benchmark | Language | #Tasks | #Questions |
| :-----: | :----: | :----: | :----: |
| [MMLU](https://openreview.net/pdf?id=d7KBjmI3GmQ) | En | 57 | 15908 |
| [AGIEval](https://arxiv.org/abs/2304.06364) | EN, Zh | 20 | 8062 |
| [MMCU](https://arxiv.org/abs/2304.12986) | Zh | 51 | 11900 |
| M3KE | Zh | 71 | 20477 |


All 71 tasks displayed according to their subjects and levels.

| | Arts Humanities | Social Sciences | Natural Sciences | Others |
| :----- | :---- | :---- | :---- | :---- |
| Primary school | Chinese |  | Math |  |
| Junior high school | Chinese, History | Politics | Math, Physics, Biology, Chemistry, Geography |  |
| High school | Chinese, History | Politics | Math, Physics, Biology, Chemistry, Geography |  |
| College | Modern History, History Foundation, Modern World History | Chinese Constitutional Law, History of Chinese Education, History of the Chinese Legal System, Developmental and Educational Psychology, History of Foreign Education, Experimental Psychology, Introduction to Psychology, Moral Cultivation, Psychology of Teaching, Principles of Pedagogy, Educational Research Methods, Current Affairs and Politics, Introduction to Mao Tsetung Thoughts, Civil Law, Jurisprudence, Sociology, Basic Principle of Marxism, Criminal Jurisprudence, Outline of Chinese Modern History | Humanistic Medicine, Internal Medicine, Animal Physiology, Surgical Sciences, Operating Systems, Data Structures, Probability Theory, Biochemistry, Biochemistry and Pathology, Physiology, Principles of Computer Composition, Computer Networks,Advanced Mathematics, Linear Algebra, Stomatology, Anthropotomy, Pharmacology, Immunology | Management, Economics |
| Others | | | Computer Grade Exam (Computer Fundamentals, Programming Languages) | Chinese Medicine, Ancient Chinese Language, Novels, Religion, Chinese Civil Service Examination |


## Evaluation Leaderboard (more models to be added)


**If you want to have your Chinese large language models assessed and added to the leaderboard, please feel free to contact us via liuc_09@tju.edu.cn or submit a pull request.**

Average zero-shot accuracy of each evaluated model on four major discipline clusters:

| Models | Arts&Humanities | Social Sciences | Nature Sciences | Others | Average |
| :-----: | :----: | :----: | :----: | :----: | :----: |
| [GLM-335M](https://aclanthology.org/2022.acl-long.26.pdf) | 0.070 | 0.046 | 0.084 | 0.044 | 0.062 |
| [Bloom-7B](https://arxiv.org/pdf/2211.05100.pdf) | 0.163 | 0.159 | 0.161 | 0.158 | 0.161 |
| [GLM-10B](https://aclanthology.org/2022.acl-long.26.pdf) | 0.180 | 0.229 | 0.219 | 0.150 | 0.197 |
| [GLM-130B](https://openreview.net/pdf?id=-Aw0rrrPUF) | 0.326 | 0.352 | 0.274 | 0.359 | 0.328 |
| [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B) | 0.246 | 0.267 | 0.168 | 0.263 | 0.236 |
| [MOSS-SFT-16B](https://github.com/OpenLMLab/MOSS) | 0.260 | 0.263 | 0.207 | 0.275 | 0.251 |
| [BEELE-7B-0.2M](https://huggingface.co/BelleGroup/BELLE-7B-0.2M) | 0.247 | 0.296 | 0.260 | 0.260 | 0.266 |
| [BEELE-7B-2M](https://huggingface.co/BelleGroup/BELLE-7B-2M) | 0.328 | 0.367 | 0.282 | 0.355 | 0.333 |
| [GPT3.5-turbo](https://platform.openai.com/docs/models/gpt-3-5) | 0.460 | 0.538 | 0.444 | 0.481 | 0.481 |


Average five-shot accuracy of each evaluated model on four major discipline clusters:

| Models | Arts&Humanities | Social Sciences | Nature Sciences | Others | Average |
| :-----: | :----: | :----: | :----: | :----: | :----: |
| [GLM-335M](https://aclanthology.org/2022.acl-long.26.pdf) | 0.220 | 0.247 | 0.193 | 0.126 | 0.196 |
| [Bloom-7B](https://arxiv.org/pdf/2211.05100.pdf) | 0.247 | 0.260 | 0.235 | 0.246 | 0.247 |
| [GLM-10B](https://aclanthology.org/2022.acl-long.26.pdf) | 0.294 | 0.304 | 0.232 | 0.211 | 0.260 |
| [GLM-130B](https://openreview.net/pdf?id=-Aw0rrrPUF) | 0.297 | 0.329 | 0.246 | 0.228 | 0.275 |
| [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B) | 0.188 | 0.175 | 0.121 | 0.198 | 0.171 |
| [MOSS-SFT-16B](https://github.com/OpenLMLab/MOSS) | 0.266 | 0.264 | 0.258 | 0.284 | 0.268 |
| [BEELE-7B-0.2M](https://huggingface.co/BelleGroup/BELLE-7B-0.2M) | 0.292 | 0.327 | 0.273 | 0.307 | 0.299 |
| [BEELE-7B-2M](https://huggingface.co/BelleGroup/BELLE-7B-2M) | 0.287 | 0.309 | 0.284 | 0.313 | 0.298 |
| [GPT3.5-turbo](https://platform.openai.com/docs/models/gpt-3-5) | - | - | - | - | - |


The '-' symbol in the table indicates ongoing testing of GPT3.5-turbo with forthcoming results.
