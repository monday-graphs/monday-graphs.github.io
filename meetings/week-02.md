---
title: "第2周 (5月11日)"
parent: 会议纪要
nav_order: 2
---

# 第2周小讨论班会议纪要

| 项目 | 内容 |
|------|------|
| 日期 | 2026年5月11日（周一） |
| 主讲人 | 路宇轩 |
| 主题 | The Lovász Conjecture holds for moderately dense Cayley graphs |
| 论文 | arXiv:2603.08675v2 |
| 作者 | Benjamin Bedert (Cambridge), Nemanja Draganić (Oxford), Alp Müyesser (Oxford), Matías Pavez-Signé (U. Chile) |

---

## 一、研究背景与动机

Lovász 猜想（1969）是组合数学中最重要的未解决问题之一，它断言：每个连通的顶点传递图都存在 Hamilton 圈。更早的 Rapaport-Strasser（1959）版本则聚焦于 Cayley 图：每个至少含 3 个元素的有限群上的连通 Cayley 图都是 Hamilton 的。

尽管已有六十余年的研究，该猜想仍然未被完全证明。已知结果包括：

- 对 Abel 群和 $p$-群成立
- 对"典型"生成集（随机选取足够多的生成元）成立
- Christofides, Hladký, Máthé（2014）证明了稠密情形：度 $d \ge \varepsilon n$ 时成立，但证明依赖 Szemerédi 正则引理，无法推广到稀疏图

## 二、论文主要贡献

本文**打破了之前的密度障碍**，证明了**多项式稀疏**的 Cayley 图也满足 Lovász 猜想：

> **定理 1.2**：存在常数 $c \ge 1/200$，使得对所有充分大的 $n$，每个度 $d > n^{1-c}$ 的 $n$ 顶点连通 Cayley 图都有 Hamilton 圈。

### 关键创新

1. **避免了 Szemerédi 正则引理**，转而使用一种专门针对 Cayley 图的**弱算术正则引理**（weak arithmetic regularity lemma，引自 Bedert 等人关于 Graham 重排猜想的工作）
2. 研发了适用于稀疏 Cayley 图的**吸收方法**（absorption method）的高效实现
3. 得到了更好的量化依赖关系（非塔式增长）

## 三、证明框架概述

证明分为四个主要步骤：

1. **Step 1 — 构造吸收结构**：在 Cayley 图中找到吸收器（absorber），利用 Cayley 图的平移不变性，通过随机平移生成大量吸收器

2. **Step 2 — 寻找线性森林**：利用 Magnant-Martin 猜想相关结果，在近正则图中用尽可能少的路径覆盖几乎所有顶点

3. **Step 3 — 连接路径**：利用无稀疏割（no sparse cut）性质保证的强连通性，将吸收器和路径森林连接成几乎张成的圈

4. **Step 4 — 吸收剩余顶点**：利用吸收器的性质将所有未覆盖的顶点纳入，完成 Hamilton 圈

### 核心定义与工具

- **$\varepsilon$-稀疏割（$\varepsilon$-sparse-cut）**：若 $V = X \cup Y$ 且 $e(X, Y) \le \varepsilon \vert X \vert \vert Y \vert$，则为稀疏割
- **弱算术正则引理（Theorem 2.2）**：存在子群 $H \le G$，使得 $\mathrm{Cay}_H(S \cap H)$ 无稀疏割
- **$H$-骨架（$H$-skeleton）**：在辅助图 $\mathrm{Aux}_{G/H}(S)$ 的 Euler 回路对应下的匹配结构
- **robust expander**：无稀疏割的图具有良好的 robust expansion 性质

## 四、讨论要点

1. **常数 $1/200$ 的局限性**：作者未尝试优化该常数，但现有方法无法突破度 $d \ge n^{1/2}$ 的门槛，因为超过此阈值弱算术正则引理不再给出有用信息

2. **未来方向**：
   - 推进到度 $d = n^{o(1)}$ 的情形
   - 研究有向 Cayley 图的稠密版本

3. **技术难点**：
   - 如何在构造吸收器时不显著破坏剩余图的度正则性
   - 如何在稀疏条件下实现路径的有效连接
   - 弱算术正则引理给出的展开条件较为温和，需要精细处理

## 五、会议信息

- 会议平台：腾讯会议
- 含屏幕共享演示
- 会议时长约 3 小时

## 视频回放

百度网盘链接：[https://pan.baidu.com/s/1iaJQGWiWTqjKMHaR6u7Igg?pwd=pb7t](https://pan.baidu.com/s/1iaJQGWiWTqjKMHaR6u7Igg?pwd=pb7t) 提取码: pb7t

文件：2026-05-11-会议视频（2）.mp4 等2个文件

## 补充笔记

（无）
