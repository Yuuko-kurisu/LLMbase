---
author: shb
icon: pen-to-square
date: 2023-06-12
shortTitle: Goat
category:
  - 大语言模型
tag:
  - 推理
star: true
---

# 在特定任务上微调语言模型

论文：Goat: Fine-tuned LLaMA Outperforms GPT-4 on Arithmetic Tasks【新加坡国立大学】

Goat模型是一个基于7B LLaMA微调的模型，在算术任务上的性能优于GPT-4，在零样本设置中还超越了75倍参数量的540B PaLM

<!-- more --> 

不过对业务来说，这篇论文也打开了专用模型的大门，毕竟大部分公司追求的都是在某一领域超越GPT-4即可。
虽然Goat并不是第一个针对特定任务进行微调的语言模型，还有大量的基于FLAN微调的工作，但Goat取得成功的两个要素在于：

1. 在一个更好的基础语言模型上，在目标任务（相对于通用预训练或指令微调）上进行有监督微调；
2. LLaMA对数字的分词技术（将每个数字单独分配一个token）

从实验结果可知二者的结合是很重要的，
第一点是因为原始7 B LLaMA基础型号不如GPT-4；
第二点是因为对OPT，GPT-J等模型的微调结果不如Goat好，因为其他模型的数字分词技术不统一。
也有人有疑问，为什么不用Wolfram Alpha或常规计算器等工具进行算数计算，而非要用语言模型算数？
对这篇论文来说，算术任务可以很容易地合成数据集，评估也更方便，方便测试微调性能。

另一个微调LLM以提高某一特定功能的例子是Gorilla，一个专门用于生成API调用的LLM。