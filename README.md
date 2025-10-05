# A Unified Two-Time-Scale Stochastic Approximation Framework for Root-Finding Bilevel Optimization

Welcome to the official repository for our paper.  
This repository contains the Jupyter Notebook with all the code necessary to reproduce the experimental results presented in our work.

---

## 📂 Repository Structure

The provided `.ipynb` notebook is organized into several sections, each corresponding to a specific figure or experiment in the paper:

* **Code Block 1: Conceptual Figure Generation (Fig. 3)**  
  - Generates the conceptual illustration from the paper.  
  - Provides an intuitive comparison of the update dynamics between the **Squared-Residual (Opt-h2)** approach and our proposed **Direct Root-Finding (TTSA)** method.  

* **Code Block 2: Experiment 1 — Synthetic Quadratic Bilevel Optimization**  
  - Implements the synthetic quadratic Root-Finding Bilevel Optimization (RF-BO) problem.  
  - **Outputs**: Figure 1(a-b), Figure 1(c-d), Table 1.  

* **Code Block 3: Experiment 2 — Adaptive Temperature Tuning in SAC**  
  - Applies TTSA to automatic tuning of the temperature parameter $\alpha$ in the Soft Actor-Critic (SAC) algorithm.  
  - **Outputs**: Figure 2, Table 2.  

* **Code Block 4: Experiment 3 — Adaptive Temperature in SimCLR Contrastive Learning**  
  - Applies TTSA to **self-supervised contrastive learning**.  
  - Dynamically tunes the **temperature** hyperparameter in the NT-Xent loss of SimCLR during training on CIFAR-10.  
  - Objective: maintain the average cosine similarity of positive pairs at a predefined target.  
  - **Outputs**: Figure 3 (three subplots), comparing:  
    1. Downstream linear classification accuracy & temperature evolution.  
    2. Two key representation metrics: **Alignment** and **Uniformity**.  
    3. Final summary of performance across methods.  

---



````markdown
## ⚙️ How to Run the Code

We recommend using conda to create an isolated virtual environment.

```bash
# 1. Create and activate environment
conda create -n ttsa_env python=3.9
conda activate ttsa_env

# 2. Install dependencies
pip install torch torchvision numpy matplotlib tqdm pandas scipy gymnasium[classic_control]

# ⚠️ Note:
# For PyTorch, please visit the official PyTorch website to find the 
# appropriate installation command for your CUDA version.

# 3. Launch Jupyter and run the notebook
jupyter notebook
````

---

## 🔁 Reproducibility Notes

* **Hyperparameters**: All hyperparameters are explicitly defined at the beginning of each code block.
* **Random Seeds**: A fixed list of random seeds is used in all experiments.
* **Hardware**: Experiments were conducted on an NVIDIA A100 GPU.

---





# Root-Finding 双层优化的统一两时间尺度随机近似框架

欢迎访问本论文的官方代码仓库。  
本仓库包含一个 Jupyter Notebook，内含复现论文中全部实验结果的代码。

---

## 📂 仓库结构

提供的 `.ipynb` 文件分为多个部分，每部分对应论文中的一个实验或图表：

* **代码块 1: 概念图生成 (图 3)**  
  - 生成论文中的概念性示意图。  
  - 直观比较 **平方残差 (Opt-h2)** 方法与我们提出的 **直接 Root-Finding (TTSA)** 方法的更新动态差异。  

* **代码块 2: 实验 1 — 合成二次双层优化**  
  - 实现合成的二次 Root-Finding 双层优化 (RF-BO) 问题。  
  - **输出**: 图 1(a-b), 图 1(c-d), 表 1。  

* **代码块 3: 实验 2 — SAC 中的温度自适应调节**  
  - 将 TTSA 应用于 Soft Actor-Critic (SAC) 算法中温度参数 $\alpha$ 的自动调节。  
  - **输出**: 图 2, 表 2。  

* **代码块 4: 实验 3 — SimCLR 对比学习中的温度自适应调节**  
  - 将 TTSA 应用于 **自监督对比学习**。  
  - 在 CIFAR-10 上训练 SimCLR 时，动态调整 NT-Xent 损失函数的 **温度** 超参数。  
  - 目标：保持正样本对的平均余弦相似度在预设目标值附近。  
  - **输出**: 图 3（三个子图），比较：  
    1. 下游线性分类准确率与温度变化。  
    2. 两个关键表示学习指标：**对齐度 (Alignment)** 与 **均匀性 (Uniformity)**。  
    3. 各方法的最终性能总结。  

---

## ⚙️ 运行方法

推荐使用 conda 创建独立虚拟环境。

```bash
# 1. 创建并激活环境
conda create -n ttsa_env python=3.9
conda activate ttsa_env

# 2. 安装依赖
pip install torch torchvision numpy matplotlib tqdm pandas scipy gymnasium[classic_control]

# ⚠️ 注意：
# PyTorch 的安装命令需根据 CUDA 版本到官网查询。

# 3. 启动 Jupyter Notebook
jupyter notebook
````

---

## 🔁 复现说明

* **超参数**: 所有超参数均在每个代码块开头显式定义。
* **随机种子**: 所有实验均使用固定的随机种子列表。
* **硬件**: 所有实验均在 NVIDIA A100 GPU 上完成。

---
