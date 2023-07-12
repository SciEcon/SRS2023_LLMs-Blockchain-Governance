# How Large Language Models Enhance Blockchain Governance: Methods and Data
## Project information
- **Author**: Yutong Quan, Political Economy/Economics, Class of 2024, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: This is a deliverable of the 2023 Summer Research Scholars (SRS) program instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: I would like to express my heartfelt gratitude to Prof. Luyao Zhang for her invaluable guidance and unwavering support throughout this project. I would also like to extend my sincere appreciation to the SciEcon editorial team, including Xintong Wu, Wanlin Deng, Xinyu Tian, and Zesen Zhuang, for their meticulous attention to detail, constructive feedback, and diligent efforts in reviewing and editing this project. I also thank the DKU 2023 SRS program, as their recognition and support have provided the necessary resources and platform for the successful execution of this research.
- **Project Summary**: 

In recent years, the deployment of Large Language Models (LLMs) has expanded across various domains, including finance, medicine, and law (Ling et al. 2023). LLMs have proven effective in tasks such as text generation and summarization, question answering, translation, topic analysis, and sentiment analysis (Trummer 2023; Yang et al. 2023; Zhao et al. 2023; Ling et al. 2023; Wang et al. 2023). Unlike traditional Natural Language Processing (NLP) models, LLMs leverage large parameters, extensive training data, and substantial computing power to perform these tasks with minimal or no specialized training (Zhao et al. 2023).

The combination of LLMs and blockchain is still in its early stages, but the research conducted by Gai et al. (2023) has made significant contributions to this interdisciplinary field. They introduced a dynamic, real-time method that utilizes LLMs to detect anomalous blockchain transactions. This approach offers several advantages, including an expansive search space and the ability to detect a broader spectrum of anomalies without depending on pre-defined rules or patterns. The proposed tool, BLOCKGPT, generates trace representations of blockchain activity and trains a large language model from scratch to serve as a real-time Intrusion Detection System. These contributions enhance blockchain security and have positive implications for the future development of decentralized systems.

Existing literature has primarily focused on utilizing LLMs to detect anomalous blockchain transactions. In contrast, our research is dedicated to exploring the potential of LLMs in enhancing social governance within blockchain networks. Through our previous literature review, we have identified the significant potential of LLMs in enhancing social governance within blockchain networks. LLMs can facilitate a more inclusive and diverse decision-making process by synthesizing and analyzing textual discussions within blockchain communities. Furthermore, LLMs can contribute to the transparency of blockchain governance by providing explanations and justifications for decisions made.
This article aims to introduce two main components. Firstly, we will present a dataset of discussions from the Uniswap community on the Discord forum. This dataset will serve as a valuable resource for training and evaluating LLMs in the context of blockchain governance. Secondly, we will demonstrate an application method utilizing h2oGPT, an open-source repository of LLMs, to apply these models to blockchain social governance.


  - **Application Scenario (Data Source)**: Blockchain Governance (Uniswap Discord *#governance* channel)
  - **Methodology**: Large Language Models (H2O.ai)

## Table of Contents
- [data](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/tree/main#data)
- [code](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/tree/main#code)
- [spotlight](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/tree/main#spotlight)
- [more about the author](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/tree/main#more-about-the-author)
- [references](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/tree/main#reference)

## Data
- Data Source: https://discord.com/channels/597638925346930701/755969053280960533
- Tool: https://github.com/Tyrrrz/DiscordChatExporter

**Data Information**

| File | Variable | Description | Unit | Type |
| ----- | --------- | ----------- | ----------- | ----------- |
| [Discord-Uniswap-Governance](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/data/Queried_Data/Discord%20-%20Uniswap%20-%20Governance.csv) | AuthorID | The ID of the author of the discussion. | none | int |
| | Author | The name of the author of the discussion. | none | object |
| | Date | The date when the discussion took place. | 1 day | object |
| | Content | The text content of the discussion. | none | object |
| | Attachments | Any attachments or files associated with the discussion. | object |
| | Reactions | The reactions or responses received for the discussion. | 1 (number) | object |

## Code
| File | Description |
| ----- | ----------- |
| [SRS2023_Discord_data_process.ipynb](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/code/SRS2023_Discord_data_process.ipynb) | Discord discussion data process and visualization |

## Spotlight
- **Discord Figures**

![1](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/discord%20screenshot.png?raw=true)
**Figure. 1: Screenshot of Uniswap Discord #governance channel.**


![2](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/discordchatexporter.png?raw=true)
**Figure. 2: DiscordChatExporter Application.**


![3](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/discord%20dataset.png?raw=true)
**Figure. 3: Uniswap Discord #governance channel discussion dataset.**


![4](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/discussion%20volume.png?raw=true)
**Figure. 4: Uniswap Discord #governance channel discussion volume.**


![5](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/word%20cloud.png?raw=true)
**Figure. 5: Uniswap Discord #governance channel discussion content word cloud.**


- **H2O.ai Figures**

![6](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/LLM%20data%20studio.png?raw=true)
**Figure. 6: H2O LLM Data Studio web interface (cited from [H2O.ai](https://h2o.ai/blog/streamlining-data-preparation-for-fine-tuning-of-large-language-models/)).**


![7](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/fine-tune.png?raw=true)
**Figure. 7: H2O LLM Studio fine-tune example (cited from [H2O.ai](https://h2o.ai/blog/effortless-fine-tuning-of-large-language-models-with-open-source-h2o-llm-studio/.)).**


![8](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/experiment%20steps.png?raw=true)
**Figure. 8: H2O LLM Studio experiment steps (cited from [H2O.ai](https://h2o.ai/blog/effortless-fine-tuning-of-large-language-models-with-open-source-h2o-llm-studio/.)).**


![9](https://github.com/SciEcon/SRS2023_LLMs-BlockchainGovernance/blob/main/spotlight/figures/h2ogpt.png?raw=true)
**Figure. 9: h2oGPT web interface (cited from [H2O.ai](https://github.com/h2oai/h2ogpt)).**

## More about the Author
![yutong](https://github.com/yutongquan/Yutong-Quan/blob/main/image/chapel%20photo.png?raw=true)

Yutong Quan is a rising senior student majoring in Political Economy with an Economics track. Interested research areas include blockchain governance, decentralized finance, and interdisciplinary fields of Artificial Intelligence and economics.

## References

### Data Source
Uniswap Discord: https://discord.com/channels/597638925346930701/755969053280960533

### Code Source
DiscordChatExporter GitHub: https://github.com/Tyrrrz/DiscordChatExporter

h2oGPT GitHub: https://github.com/h2oai/h2ogpt

H2O LLM Studio: https://github.com/h2oai/h2o-llmstudio

### Articles
H2O.ai. 2023a. “Effortless Fine-Tuning of Large Language Models with Open-Source H2O LLM Studio.” H2O.ai. May 1, 2023. https://h2o.ai/blog/effortless-fine-tuning-of-large-language-models-with-open-source-h2o-llm-studio/.

———. 2023b. “Streamlining Data Preparation for Fine Tuning of Large Language Models.” H2O.ai. June 14, 2023. https://h2o.ai/blog/streamlining-data-preparation-for-fine-tuning-of-large-language-models/.
