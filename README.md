# Awesome LLM-RLVR [🔥📜]

<div align="center">
  <a href="https://github.com/PKU-Fgx/RLVR-Survey/stargazers"><img src="https://img.shields.io/github/stars/PKU-Fgx/RLVR-Survey?style=for-the-badge" alt="Stargazers"></a>
  <a href="https://github.com/PKU-Fgx/RLVR-Survey/network/members"><img src="https://img.shields.io/github/forks/sPKU-Fgx/RLVR-Survey?style=for-the-badge" alt="Forks"></a>
  <a href="https://github.com/PKU-Fgx/RLVR-Survey/graphs/contributors"><img src="https://img.shields.io/github/contributors/PKU-Fgx/RLVR-Survey?style=for-the-badge" alt="Contributors"></a>
  <a href="https://github.com/PKU-Fgx/RLVR-Survey/blob/main/LICENSE"><img src="https://img.shields.io/github/license/PKU-Fgx/RLVR-Survey?style=for-the-badge" alt="MIT License"></a>
</div>

>  一份精选的研究论文、工具、数据集和框架列表，用于大语言模型（LLMs）中具有**可验证奖励的强化学习**（Reinforcement Learning with Verifiable Rewards, RLVR）。
> 受基础模型在对齐、推理与自我改进三者交叉领域的启发。 

<details>
  <summary>🗂️ 目录 </summary>
  <ol>
    <li><a href="#motivation">🌟 Motivation</a></li>
    <li><a href="#auto-fetched-recent-papers">🔄 Auto-Fetched Recent Papers</a></li>
    <li><a href="#core-papers">🧠 Core Papers</a></li>
    <li><a href="#unsupervised-rlvr">🔍 Unsupervised RLVR</a></li>
    <li><a href="#entropy-in-rlvr">📉 Entropy in RLVR</a></li>
    <li><a href="#rlvr-analysis">🧪 RLVR Analysis</a></li>
    <li><a href="#mllm">🖼️ Multimodal LLM</a></li>
    <li><a href="#evaluation">📏 Evaluation Issue</a></li>
    <li><a href="#blogs">📰 Awesome Blogs about RLVR</a></li>
    <li><a href="#toolkits-and-libraries">🛠️ Toolkits and Libraries</a></li>
    <li><a href="#star">⭐ Star History</a></li>
    <li><a href="#contributing">🤝 Contributing</a></li>
    <li><a href="#license">🧾 License</a></li>
  </ol>
</details>

---

<h2 id="motivation">🌟 Motivation</h2>

RLVR 是一种快速发展的范式，通过外部奖励验证、自洽性和自举学习来对齐大语言模型（LLMs），使模型能够在不过度依赖人工监督的情况下提升推理能力。

---

### 🔄 Auto-Fetched Recent Papers



<h2 id="core-papers">🧠 Core Papers</h2>

<h3 id="rlvr-foundations">RLVR Foundations</h3>

<h4>2025</h4>

1. 👉【高效推理】**Optimizing Anytime Reasoning via Budget Relative Policy Optimization.**   <2025.06>      
    [[Paper]](https://arxiv.org/abs/2505.13438)    *Sea AI、新加坡国立*   
    > 在这项工作中，我们提出了一个新框架 AnytimeReasoner，用于优化“随时推理”（anytime reasoning）性能，目标是在不同 token 预算约束下提高 token 效率和推理灵活性。为此，我们从一个先验分布中采样 token 预算，并将完整的思维过程截断到这些预算长度，迫使模型为每段截断的思维生成可验证的最佳答案，以此引入可验证的密集奖励，从而在强化学习优化中实现更有效的信用分配。
   
2. 👉【改进 RLVR 范式】**Language Models Can Learn from Verbal Feedback Without Scalar Rewards.**   <2025.09>      
    [[Paper]](https://arxiv.org/abs/2509.22638)    *Sea AI*   
    > 我们提出将口头反馈视为一种条件信号，而不是压缩为单一的数值奖励。

3. 👉【高效推理】**Entropy After $\textlangle$ `/Think` $\textrangle$ for reasoning model early exiting.**   <2025.09>      
    [[Paper]](https://arxiv.org/abs/2509.26522)    *Netflix Research*   
    > 为检测并防止过度思考，我们提出了一种简单且廉价的信号 —— “`</Think>` 之后的熵（Entropy After `</Think>`, EAT）” —— 用于监控并决定是否提前退出推理。
    
4. 👉【RLVR 原理】**Response-Level Rewards Are All You Need for Online Reinforcement Learning in LLMs: A Mathematical Perspective.**  <2025.06>      
    [[Paper]](https://www.arxiv.org/abs/2506.02553)    *Amazon*   
   > 在本文中，我们提出了统一的理论视角，我们引入了**轨迹策略梯度定理（Trajectory Policy Gradient Theorem）**，表明无论零奖励假设是否成立，在 REINFORCE 和 Actor-Critic 一类算法中，只用 整条回应的最终奖励（response-level reward） 就可以对真实、未知的 token-级奖励进行无偏估计。

5. 👉【数据高效】**Towards High Data Efficiency in Reinforcement Learning with Verifiable Reward.**  <2025.09>      
    [[Paper]](https://www.arxiv.org/abs/2509.01321)    *人大、阿里蚂蚁*   
   > 近期的大型推理模型研究利用带可验证奖励的强化学习（RLVR）来提升模型的推理能力。然而，这类方法要做到大规模训练通常需要大量的 rollout 计算以及巨大的数据集，从而导致训练成本高、数据效率低。为了解决这个问题，本论文提出了 DEPO（Data-Efficient Policy Optimization） —— 一种数据高效的策略优化管道，它结合了离线和在线数据选择的优化策略。

6. 👉【改进 RLVR 范式】**Act Only When It Pays: Efficient Reinforcement Learning for LLM Reasoning via Selective Rollouts.** <2025.06>   
   [[Paper]](https://www.arxiv.org/abs/2506.02177) [[Code]](https://github.com/Infini-AI-Lab/GRESO/)    *Carnegie Mellon、Meta*  
   > 尽管带有可验证奖励的强化学习（Reinforcement Learning with Verifiable Rewards, RLVR）已成为发展大型语言模型高级推理能力的重要组成部分，但现有研究表明，在经过数千次优化步骤后训练会出现性能停滞（即“平台期”），即使增加计算资源也难以获得显著性能提升。造成这一限制的原因是当前 RLVR 训练中探索非常稀疏 —— 模型依赖有限的 rollout（执行轨迹）经常错过关键的推理路径，无法系统覆盖解空间。   
   > 我们提出了 DeepSearch，一个将**蒙特卡洛树搜索（Monte Carlo Tree Search, MCTS**直接集成进 RLVR 训练的框架。与现有方法仅在推理（inference）过程中使用树搜索不同，DeepSearch 把结构化搜索嵌入训练循环，实现了针对推理步骤的系统性探索和细粒度的奖励（credit）分配。   

7. 👉【改进 RLVR 范式】**Let it Calm: Exploratory Annealed Decoding for Verifiable Reinforcement Learning.** <2025.06>   
   [[Paper]](https://www.arxiv.org/abs/2510.05251)    *University of Chicago、Meta*  
   > 在本文中，作者提出了一种更简单且更有效的策略——探索性退火解码（Exploratory Annealed Decoding, EAD）。该方法基于一个核心洞察：**在序列生成过程中，早期 token 对整个序列的语义方向最关键，因此探索性在早期更有价值。**    
     EAD 采用了“先探索、后利用（explore-at-the-beginning, exploit-at-the-end）”的动态温度策略——从较高温度逐步退火到较低温度。  

8. 👉【改进 GRPO】**KDRL: Post-Training Reasoning LLMs via Unified Knowledge Distillation and Reinforcement Learning.** <2025.06>  
    [[Paper]](https://arxiv.org/pdf/2506.02208v1)    *哈工大*
   >本文提出了 KDRL，一种 统一的后训练框架，通过教师监督（KD）和模型自身探索（RL）共同优化推理模型。具体而言，KDRL 使用策略梯度优化，同时最小化学生模型与教师模型分布的逆向 Kullback–Leibler 散度（RKL），并最大化基于规则的预期奖励。论文构建了一个将 GRPO（Group Relative Policy Optimization） 与 KD 结合的统一目标，并系统性地研究了不同 KL 近似方法、KL 权重系数以及基于奖励指导的 KD 策略对训练动态和性能的影响。
   
9. 👉【改进 GRPO】**Rewarding the Unlikely: Lifting GRPO Beyond Distribution Sharpening.** <2025.06>  
    [[Paper]](https://www.arxiv.org/abs/2506.02355)    *Carnegie Mellon University.*  
   > 为了解决 GRPO 的排序偏差，我们提出了 unlikeliness reward（不太可能性奖励），一种显式提高低概率正确结果权重的方法。我们展示了不太可能性奖励可以缓解排序偏差，并在合成和真实的定理证明设置中，在多个 N 值下提高 pass@N 表现。
   
10. 👉【RLVR 是否能拓展能力边界】**The Invisible Leash: Why RLVR May or May Not Escape Its Origin.** <2025.09>  
    [[Paper]](https://www.arxiv.org/abs/2507.14843)    *Stanford University、NVIDIA*  
   > 本研究通过理论和大规模实证研究揭示了 RLVR 可能的局限性。我们发现，在当前训练条件下，RLVR 的优化往往像一种 受基座模型支持集限制的保守性重加权机制，这可能限制完全原创解的发现，并使优化受限于基座模型的初始分布。我们还识别出一个 熵与奖励之间的权衡：虽然现有的 RLVR 方案可靠地提升了精度，但它也可能逐步缩小探索范围，从而遗漏那些正确但概率较低的解。

11.  **Critique-GRPO: Advancing LLM Reasoning with Natural Language and Numerical Feedback** <2025.06>  
    *Xiaoying Zhang, Hao Sun, Yipeng Zhang, Kaituo Feng, Chaochao Lu, Chao Yang, Helen Meng* **arXiv**    
   [[Paper]](https://www.arxiv.org/abs/2506.03106) [[Code]](https://github.com/zhangxy-2019/critique-GRPO)
12. **Beyond Markovian: Reflective Exploration via Bayes-Adaptive RL for LLM Reasoning.** <2025.05>  
   *Shenao Zhang, Yaqing Wang, Yinxiao Liu, Tianqi Liu, Peter Grabowski, Eugene Ie, Zhaoran Wang, Yunxuan Li.* **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.20561)
13. **S-GRPO: Early Exit via Reinforcement Learning in Reasoning Models.** <2025.05>  
    *Muzhi Dai, Chenxu Yang, Qingyi Si.* **arXiv**  
   [[Paper]](https://arxiv.org/abs/2505.07686)
14. **Temporal Sampling for Forgotten Reasoning in LLMs** <2025.05>   
   *Yuetai Li, Zhangchen Xu, Fengqing Jiang, Bhaskar Ramasubramanian, Luyao Niu, Bill Yuchen Lin, Xiang Yue, Radha Poovendran.* **arXiv**    
   [[Paper]](https://arxiv.org/abs/2505.20196) [[Code]](https://github.com/uw-nsl/Temporal_Forgetting)
15. **DAPO: An Open-Source LLM Reinforcement Learning System at Scale.**  <2025.05>   
   *Yu et al.* **arXiv**    
   [[Paper]](https://arxiv.org/abs/2503.14476) [[Code]](https://github.com/BytedTsinghua-SIA/DAPO)
16. **RM-R1: Reward Modeling as Reasoning**  <2025.05>  
    *Xiusi Chen, Gaotang Li, Ziqi Wang, Bowen Jin, Cheng Qian, Yu Wang, Hongru Wang, Yu Zhang, Denghui Zhang, Tong Zhang, Hanghang Tong, Heng Ji.* **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.02387) [[Code]](https://github.com/RM-R1-UIUC/RM-R1)
17. **GRPO-LEAD: A Difficulty-Aware Reinforcement Learning Approach for Concise Mathematical Reasoning in Language Models.**  <2025.04>   
    *Jixiao Zhang, Chunsheng Zuo.* **arXiv**   
    [[Paper]](https://arxiv.org/abs/2504.09696)
18. **VAPO: Efficient and Reliable Reinforcement Learning for Advanced Reasoning Tasks.** <2025.04>
    *Yu Yue, Yufeng Yuan, Qiying Yu, Xiaochen Zuo, Ruofei Zhu, Wenyuan Xu, Jiaze Chen, Chengyi Wang, TianTian Fan, Zhengyin Du, Xiangpeng Wei, Xiangyu Yu, Gaohong Liu, Juncai Liu, Lingjun Liu, Haibin Lin, Zhiqi Lin, Bole Ma, Chi Zhang, Mofan Zhang, Wang Zhang, Hang Zhu, Ru Zhang, Xin Liu, Mingxuan Wang, Yonghui Wu, Lin Yan.* **arXiv**
    [Paper]()
19. **Online Difficulty Filtering for Reasoning Oriented Reinforcement Learning.**  <2025.04>   
    *Sanghwan Bae, Jiwoo Hong, Min Young Lee, Hanbyul Kim, JeongYeon Nam, Donghyun Kwak.*  **arXiv**   
    [[Paper]](https://arxiv.org/abs/2504.03380)
20. **SRPO: A Cross-Domain Implementation of Large-Scale Reinforcement Learning on LLM.** <2025.04>   
    *Xiaojiang Zhang, Jinghui Wang, Zifei Cheng, Wenhao Zhuang, Zheng Lin, Minglei Zhang, Shaojie Wang, Yinghan Cui, Chao Wang, Junyi Peng, Shimiao Jiang, Shiqi Kuang, Shouyu Yin, Chaohang Wen, Haotian Zhang, Bin Chen, Bing Yu.*  **arXiv**   
    [[Paper]](https://arxiv.org/abs/2504.14286)
21. **DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning.**  <2025.01>  
    *DeepSeek-AI.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2501.12948)
22. **ProRL: Prolonged Reinforcement Learning Expands Reasoning Boundaries in Large Language Models.**  <2025.05>  
    *Mingjie Liu, Shizhe Diao, Ximing Lu, Jian Hu, Xin Dong, Yejin Choi, Jan Kautz, Yi Dong.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.24864)
23. **GHPO: Adaptive Guidance for Stable and Efficient LLM Reinforcement Learning.**  <2025.07>  
    *Ziru Liu, Cheng Gong, Xinyu Fu, Yaofang Liu, Ran Chen, Shoubo Hu, Suiyun Zhang, Rui Liu, Qingfu Zhang, Dandan        Tu.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2507.10628)
24. **GPG: A Simple and Strong Reinforcement Learning Baseline for Model Reasoning.**  <2025.04>  
    *Xiangxiang Chu, Hailang Huang, Xiao Zhang, Fei Wei, Yong Wang.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2504.02546)
25. **SeRL: Self-Play Reinforcement Learning for Large Language Models with Limited Data.**  <2025.05>  
    *Wenkai Fang, Shunyu Liu, Yang Zhou, Kongcheng Zhang, Tongya Zheng, Kaixuan Chen, Mingli Song, Dacheng Tao.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.20347)
26. **SPEED-RL: Faster Training of Reasoning Models via Online Curriculum Learning.**  <2025.06>  
    *Ruiqi Zhang, Daman Arora, Song Mei, Andrea Zanette.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2506.09016)
27. **Bingo: Boosting Efficient Reasoning of LLMs via Dynamic and Significance-based Reinforcement Learning.**  <2025.06>  
    *Hanbing Liu, Lang Cao, Yuanyi Ren, Mengyu Zhou, Haoyu Dong, Xiaojun Ma, Shi Han, Dongmei Zhang.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2506.08125)
28. **Reinforcement Pre-Training.**  <2025.06>  
    *Qingxiu Dong, Li Dong, Yao Tang, Tianzhu Ye, Yutao Sun, Zhifang Sui, Furu Wei.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2506.08007)
29. **Reinforcement Learning with Verifiable Rewards: GRPO’s Effective Loss, Dynamics, and Success Amplification.**  <2025.03>  
    *Youssef Mroueh.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2503.06639)

<h4>2024</h4>

1. **DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models** <2024.02>  
   *Zhihong Shao, Peiyi Wang, Qihao Zhu, Runxin Xu, Junxiao Song, Xiao Bi, Haowei Zhang, Mingchuan Zhang, Y.K. Li, Y. Wu, Daya Guo.* **arXiv**   
    [[Paper]](https://arxiv.org/abs/2402.03300) [[Code]](https://github.com/deepseek-ai/DeepSeek-Math)
2. **ReFT: Reasoning with Reinforced Fine-Tuning** <2024.01>  
   *Trung Quoc Luong, Xinbo Zhang, Zhanming Jie, Peng Sun, Xiaoran Jin, Hang Li.* **arXiv / ACL 2024**  
   [[Paper]](https://arxiv.org/abs/2401.08967) [[Code]](https://github.com/lqtrung1998/mwp_ReFT)


---

<h3 id="rlvr-foundations">Unsupervised RLVR</h3>

<h4>2025</h4>

1. **Can Large Reasoning Models Self-Train?** <2025.05> 
    *Sheikh Shafayat, Fahim Tajwar, Ruslan Salakhutdinov, Jeff Schneider, Andrea Zanette.* **arXiv**   
    [[Paper]](https://arxiv.org/abs/2505.21444) 
2. **Right Question is Already Half the Answer: Fully Unsupervised LLM Reasoning Incentivization. **    <2025.05>   
    *Qingyang Zhang, Haitao Wu, Changqing Zhang, Peilin Zhao, Yatao Bian.*     **arXiv**
    [[Paper]](https://arxiv.org/abs/2504.05812)  
4.  **Maximizing Confidence Alone Improves Reasoning**  <2025.05>     
    *Mihir Prabhudesai, Lili Chen, Alex Ippoliti, Katerina Fragkiadaki, Hao Liu, Deepak Pathak.*   **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.22660)
5.  **Learning to Reason without External Rewards.**   **arXiv**
    *Xuandong Zhao, Zhewei Kang, Aosong Feng, Sergey Levine, Dawn Song.*      **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.19590)
6. **NOVER: Incentive Training for Language Models via Verifier-Free Reinforcement Learning.**  <2025.05>  
    *Wei Liu, Siya Qi, Xinyu Wang, Chen Qian, Yali Du, Yulan He.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.16022)
7. **Absolute Zero: Reinforced Self-Play Reasoning with Zero Data.**  <2025.05>  
    *Andrew Zhao et al.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.03335)
---

<h3 id="rlvr-foundations">Entropy in RLVR</h3>

<h4>2025</h4>

1. **Beyond the 80/20 Rule: High-Entropy Minority Tokens Drive Effective Reinforcement Learning for LLM Reasoning** <2025.06>  
    *Shenzhi Wang, Le Yu, Chang Gao, Chujie Zheng, Shixuan Liu, Rui Lu, Kai Dang, Xionghui Chen, Jianxin Yang, Zhenru Zhang, Yuqiong Liu, An Yang, Andrew Zhao, Yang Yue, Shiji Song, Bowen Yu, Gao Huang, Junyang Lin.* **arXiv**    
    [[Paper]](https://arxiv.org/abs/2506.01939)
2. **The Entropy Mechanism of Reinforcement Learning for Reasoning Language Models.** <2025.05>   
    *Ganqu Cui, Yuchen Zhang, Jiacheng Chen, Lifan Yuan, Zhi Wang, Yuxin Zuo, Haozhan Li, Yuchen Fan, Huayu Chen, Weize Chen, Zhiyuan Liu, Hao Peng, Lei Bai, Wanli Ouyang, Yu Cheng, Bowen Zhou, Ning Ding.* **arXiv**    
    [[Paper]](https://arxiv.org/abs/2505.22617) [[Code]](https://github.com/PRIME-RL/Entropy-Mechanism-of-RL)
3. **One-shot Entropy Minimization.** <2025.05>  
    *Zitian Gao, Lynx Chen, Joey Zhou, Bryan Dai.* **arXiv**  
   [[Paper]](https://www.arxiv.org/pdf/2505.20282) [[Code]](https://github.com/zitian-gao/one-shot-em)
4. **The Unreasonable Effectiveness of Entropy Minimization in LLM Reasoning.** <2025.05>  
   *Shivam Agarwal, Zimin Zhang, Lifan Yuan, Jiawei Han, Hao Peng.* **arXiv**  
   [[Paper]](https://arxiv.org/abs/2505.15134)
5. **FR3E: First Return, Entropy-Eliciting Explore.**  <2025.07>  
   *Tianyu Zheng, Tianshun Xing, Qingshui Gu, Taoran Liang, Xingwei Qu, Xin Zhou, Yizhi Li, Zhoufutu Wen, Chenghua Lin, Wenhao Huang, Qian Liu, Ge Zhang, Zejun Ma*  **arXiv**  
   [[Paper]](https://arxiv.org/abs/2507.07017)
6. **Pass@k Training for Adaptively Balancing Exploration and Exploitation of Large Reasoning Models.**  <2025.08>  
   *Zhipeng Chen, Xiaobo Qin, Youbin Wu, Yue Ling, Qinghao Ye, Wayne Xin Zhao, Guang Shi.*  **arXiv**  
   [[Paper]](https://arxiv.org/abs/2508.10751)
---

<h3 id="rlvr-analysis">RLVR Analysis</h3>

<h4>2025</h4>

1. **Spurious Rewards: Rethinking Training Signals in RLVR.**  <2025.05>  
    *Rulin Shao, Shuyue Stella Li, Rui Xin, Scott Geng, Yiping Wang, Sewoong Oh, Simon Shaolei Du, Nathan Lambert, Sewon Min, Ranjay Krishna, Yulia Tsvetkov, Hannaneh Hajishirzi, Pang Wei Koh, Luke Zettlemoyer.*  **Preprint**  
    [[Paper]](https://github.com/ruixin31/Rethink_RLVR/blob/main/paper/rethink-rlvr.pdf) [[Code]](https://github.com/ruixin31/Rethink_RLVR)
2. **Reinforcement Learning Finetunes Small Subnetworks in Large Language Models.**  <2025.05>  
    *Sagnik Mukherjee, Lifan Yuan, Dilek Hakkani-Tur, Hao Peng.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2505.11711)
3. **Does Reinforcement Learning Really Incentivize Reasoning Capacity in LLMs Beyond the Base Model?**  <2025.04>  
    *Yang Yue, Zhiqi Chen, Rui Lu, Andrew Zhao, Zhaokai Wang, Shiji Song, Gao Huang.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2504.13837) [[Code]](https://github.com/LeapLabTHU/limit-of-RLVR)
4. **The Surprising Effectiveness of Negative Reinforcement in LLM Reasoning.**  <2025.06>  
    *Xinyu Zhu, Mengzhou Xia, Zhepei Wei, Wei-Lin Chen, Danqi Chen, Yu Meng.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2506.01347) [[Code]](https://github.com/TianHongZXY/RLVR-Decomposed)
5. **Reasoning or Memorization? Unreliable Results of Reinforcement Learning Due to Data Contamination.**  <2025.07>  
    *Mingqi Wu, Zhihao Zhang, Qiaole Dong, Zhiheng Xi, Jun Zhao, Senjie Jin, Xiaoran Fan, Yuhao Zhou, Huijie Lv, Ming Zhang, Yanwei Fu, Qin Liu, Songyang Zhang, Qi Zhang.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2507.10532)
6. **One Token to Fool LLM-as-a-Judge.**  <2025.07>  
    *Yulai Zhao, Haolin Liu, Dian Yu, S. Y. Kung, Haitao Mi, Dong Yu.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2507.08794)

---
<h3 id="mllm">Multimodal LLM</h3>

<h4>2025</h4>

1. *SRPO: Enhancing Multimodal LLM Reasoning via Reflection-Aware Reinforcement Learning.***  <2025.06> 
    *Zhongwei Wan, Zhihao Dou, Che Liu, Yu Zhang, Dongfei Cui, Qinjian Zhao, Hui Shen, Jing Xiong, Yi Xin, Yifan Jiang, Yangfan He, Mi Zhang, Shen Yan.*   **arXiv**   
    [[Paper]](https://arxiv.org/abs/2506.01713) [[Code]](https://srpo.pages.dev/)
2. **R1-Omni: Explainable Omni-Multimodal Emotion Recognition with Reinforcement Learning** <2025.05>   
    *Jiaxing Zhao, Xihan Wei, Liefeng Bo*  **arXiv**   
    [[Paper]](https://arxiv.org/abs/2503.05379) [[Code]](https://github.com/HumanMLLM/R1-Omni)
3. **R1-VL: Learning to Reason with Multimodal Large Language Models via Step-Wise GRPO.**  <2025.03>  
   *Jingyi Zhang, Jiaxing Huang, Huanjin Yao, Shunyu Liu, Xikun Zhang, Shijian Lu, Dacheng Tao.*  **arXiv**  
   [[Paper]](https://arxiv.org/abs/2503.12937)
4. **VL-Rethinker: Incentivizing Self-Reflection of Vision-Language Models with Reinforcement Learning.**  <2025.04>  
   *Haozhe Wang, Chao Qu, Zuming Huang, Wei Chu, Fangzhen Lin, Wenhu Chen.*  **arXiv**  
   [[Paper]](https://arxiv.org/abs/2504.08837)
5. **GTR: Guided Thought Reinforcement Prevents Thought Collapse in RL-based VLM Agent Training.**  <2025.03>  
   *Tong Wei, Yijun Yang, Junliang Xing, Yuanchun Shi, Zongqing Lu, Deheng Ye.*  **arXiv**  
   [[Paper]](https://arxiv.org/abs/2503.08525)

---
<h3 id="evaluation">Evaluation Issue </h3>

<h4>2025</h4>

1. **A Sober Look at Progress in Language Model Reasoning: Pitfalls and Paths to Reproducibility.**  <2025.04>  
    *Andreas Hochlehnert, Hardik Bhatnagar, Vishaal Udandarao, Samuel Albanie, Ameya Prabhu, Matthias Bethge.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2504.07086)
2. **Incorrect Baseline Evaluations Call into Question Recent LLM-RL Claims.**  <2025.05>  
    *Nikhil Chandak, Shashwat Goel, Ameya Prabhu.*  **Blog**  
    [[Paper]](https://safe-lip-9a8.notion.site/Incorrect-Baseline-Evaluations-Call-into-Question-Recent-LLM-RL-Claims-2012f1fbf0ee8094ab8ded1953c15a37)
3. **Evaluation is All You Need: Strategic Overclaiming of LLM Reasoning Capabilities Through Evaluation Design.**  <2025.06>  
    *Lin Sun, Weihong Lin, Jinzhu Wu, Yongfu Zhu, Xiaoqi Jian, Guangxiang Zhao, Linglin Zhang, Sai-er Hu, Yuhan Wu, Xiangzheng Zhang.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2506.04734)
4. **AbstentionBench: Reasoning LLMs Fail on Unanswerable Questions.**  <2025.06>  
    *Polina Kirichenko, Shauli Ravfogel, Roee Aharoni, Yonatan Belinkov.*  **arXiv**  
    [[Paper]](https://arxiv.org/abs/2506.09038)
5. **IFBench: Generalizing Verifiable Instruction Following.**  <2025.07>  
   *Valentina Pyatkin, Saumya Malik, Victoria Graf, Hamish Ivison, Shengyi Huang, Pradeep Dasigi, Nathan Lambert, Hannaneh Hajishirzi.*  **arXiv**  
   [[Paper]](https://arxiv.org/abs/2507.02833) [[Code]](https://github.com/allenai/if-bench)
 
--- 

<h2 id="blogs">📚 Awesome Blogs about RLVR</h2>

[SemiAnalysis](https://semianalysis.com/2025/06/08/scaling-reinforcement-learning-environments-reward-hacking-agents-scaling-data/): 
Scaling Reinforcement Learning: Environments, Reward Hacking, Agents, Scaling Data.    


---

[//]: # ([//]: # &#40;&#41;)
[//]: # ([//]: # &#40;<h2 id="surveys-and-theory">📚 Surveys and Theory</h2>&#41;)
[//]: # ()
[//]: # ()
[//]: # (<h2 id="datasets-and-benchmarks">🏗️ Datasets and Benchmarks</h2>)

[//]: # ()
[//]: # (---)

<h2 id="toolkits-and-libraries">🛠️ Toolkits and Libraries</h2>

- 【[open-r1](https://github.com/huggingface/open-r1)】-- Fully open reproduction of DeepSeek-R1. ![GitHub Stars](https://img.shields.io/github/stars/huggingface/open-r1?style=social)
- 【[PRIME](https://github.com/PRIME-RL/PRIME)】 -- Scalable RL solution for advanced reasoning of language models.  ![GitHub Stars](https://img.shields.io/github/stars/PRIME-RL/PRIME?style=social)
- 【[simpleRL-reason](https://github.com/hkust-nlp/simpleRL-reason)】 -- Simple RL training for reasoning.  ![GitHub Stars](https://img.shields.io/github/stars/hkust-nlp/simpleRL-reason?style=social)
- 【[TinyZero](https://github.com/Jiayi-Pan/TinyZero)】 -- Minimal reproduction of DeepSeek R1-Zero. ![GitHub Stars](https://img.shields.io/github/stars/Jiayi-Pan/TinyZero?style=social)
- 【[OpenR](https://github.com/openreasoner/openr)】 -- OpenR: An Open Source Framework for Advanced Reasoning with LLMs![GitHub Stars](https://img.shields.io/github/stars/openreasoner/openr?style=social)
- 【[verl](https://github.com/volcengine/verl)】 -- verl: Volcano Engine Reinforcement Learning for LLMs. ![GitHub Stars](https://img.shields.io/github/stars/volcengine/verl?style=social)
- 【[rl](https://github.com/pytorch/rl)】 -- A modular, primitive-first, python-first PyTorch library for Reinforcement Learning. ![GitHub Stars](https://img.shields.io/github/stars/pytorch/rl?style=social)
- 【[all-rl-algorithms](https://github.com/FareedKhan-dev/all-rl-algorithms)】 -- Implementation of all RL algorithms in a simpler way. ![GitHub Stars](https://img.shields.io/github/stars/FareedKhan-dev/all-rl-algorithms?style=social)
- 【[AReaL](https://github.com/inclusionAI/AReaL)】 -- Distributed RL System for LLM Reasoning. ![GitHub Stars](https://img.shields.io/github/stars/inclusionAI/AReaL?style=social)
- 【[rllm](https://github.com/agentica-project/rllm)】 -- Democratizing Reinforcement Learning for LLMs. ![GitHub Stars](https://img.shields.io/github/stars/agentica-project/rllm?style=social)
- 【[MARTI](https://github.com/TsinghuaC3I/MARTI)】 -- A Framework for LLM-based Multi-Agent Reinforced Training and Inference.  ![GitHub Stars](https://img.shields.io/github/stars/TsinghuaC3I/MARTI?style=social)
- 【[OpenRLHF](https://github.com/OpenRLHF/OpenRLHF) 】-- An Easy-to-use, Scalable and High-performance RLHF Framework based on Ray. ![GitHub Stars](https://img.shields.io/github/stars/OpenRLHF/OpenRLHF?style=social)
- 【[ROLL](https://github.com/alibaba/ROLL)】-- An Efficient and User-Friendly Scaling Library for Reinforcement Learning with Large Language Models. ![GitHub Stars](https://img.shields.io/github/stars/alibaba/ROLL?style=social)

<h2>💡 Other Awesome Lists</h2>

- **[Awesome-RL-based-LLM-Reasoning](https://github.com/bruno686/Awesome-RL-based-LLM-Reasoning)** Materials that enhance LLM reasoning with reinforcement learning. 
- **[Awesome-LLM-Reasoning](https://github.com/atfortes/Awesome-LLM-Reasoning)**  Curated collection of papers and resources on how to unlock the reasoning ability of LLMs and MLLMs.
- **[Awesome-Controllable-Generation](https://github.com/atfortes/Awesome-Controllable-Generation)**  Collection of papers and resources on Controllable Generation using Diffusion Models.
- **[Chain-of-ThoughtsPapers](https://github.com/Timothyxxx/Chain-of-ThoughtsPapers)**  A trend starting from "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models".
- **[LM-reasoning](https://github.com/jeffhj/LM-reasoning)**  Collection of papers and resources on Reasoning in Large Language Models.
- **[Prompt4ReasoningPapers](https://github.com/zjunlp/Prompt4ReasoningPapers)**  Repository for the paper "Reasoning with Language Model Prompting: A Survey".
- **[ReasoningNLP](https://github.com/FreedomIntelligence/ReasoningNLP)**  Paper list on reasoning in NLP.
- **[Awesome-LLM](https://github.com/Hannibal046/Awesome-LLM)**  Curated list of Large Language Model.
- **[Awesome LLM Self-Consistency](https://github.com/SuperBruceJia/Awesome-LLM-Self-Consistency)**  Curated list of Self-consistency in Large Language Models.
- **[Deep-Reasoning-Papers](https://github.com/floodsung/Deep-Reasoning-Papers)**  Recent Papers including Neural-Symbolic Reasoning, Logical Reasoning, and Visual Reasoning.

<p align="right" style="font-size: 14px; color: #555; margin-top: 20px;">
    <a href="#top" style="text-decoration: none; color: #007bff; font-weight: bold;">
        ↑ Back to Top ↑
    </a>
</p>
