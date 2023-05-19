# GPT2-3.5B-chinese-ft

在Colab上面进行游玩： <a href="https://colab.research.google.com/github/Midkey/GPT2-3.5B-chinese-ft/blob/main/GPT2_3_5B_chinese_ft_luotuo.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>


这是一个简单的微调项目，用于测试gpt模型。

## 预训练模型

这里预训练的模型使用的  [IDEA-CCNL/Wenzhong2.0-GPT2-3.5B-chinese](1https://huggingface.co/IDEA-CCNL/Wenzhong2.0-GPT2-3.5B-chinese)  的预训练模型。
该模型使用了悟道数据集预训练，具有基本的中文处理能力。

因此使用这个模型作为微调的预训练权重。

##finetune数据

微调的数据使用Luotuo项目中的翻译数据以及其他项目提供的数据。具体训练文件名以及所含指令数量如下包含：

|Dataset Name| Instruction Number|
|--| -- |
| luotuo_all_data.json              |         168886 |
| alpaca_gpt4_data_zh.json          |         48818 | 
| coig_data.json                    |         165531 |
| baike_all_data_rs150000.json      |         150000 |
| web_text_all_data_rs150000.json   |         150000 |

- Luotuo_all是骆驼项目收集的部分翻译数据。
- alpaca_gpt4_data_zh 从这里进行[下载](https://huggingface.co/datasets/shibing624/alpaca-zh)


后三个数据集参考的[pandallm](https://github.com/dandelionsllm/pandallm)的数据集，并进行了重新整理与采样。
- [Chinese Open Instruction Generalist (COIG)](https://huggingface.co/datasets/BAAI/COIG)
- [百科问答(baike2018qa)，150万个带问题类型的问答](https://github.com/brightmart/nlp_chinese_corpus)
- [社区问答json版(webtext2019zh)社区问答json版(webtext2019zh)](https://github.com/brightmart/nlp_chinese_corpus)

## finetune代码

微调代码使用的[Llama-x](https://github.com/AetherCortex/Llama-X), 并进行相应的修改。

## TODO:
- [ ] 尝试1B参数量的GPT模型finetune以后的性能。




