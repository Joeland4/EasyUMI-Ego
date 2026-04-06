# EasyUMI-Ego

[English](README.md) · **简体中文**

**具身智能数据采集优化框架** — 面向 **UMI** 与 **EGO（第一人称 / 可穿戴）** 两类主流具身数据采集与对齐场景，配套静态项目主页便于展示与分享。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Pages](https://img.shields.io/badge/GitHub-Pages-222?logo=github)](https://joeland4.github.io/EasyUMI-Ego/)

---

## 目录

- [项目简介](#项目简介)
- [背景与动机](#背景与动机)
- [可视化演示](#可视化演示)
- [核心方向](#核心方向)
- [项目优势](#项目优势)
- [适用场景](#适用场景)
- [开源与许可](#开源与许可)

---

## 项目简介

本项目围绕 **UMI** 与 **EGO** 两条具身智能数据路线，在 **采集成本**、**机械臂适配** 与 **数据可用性** 等方向做系统化优化，便于在消费级硬件条件下获得可用于机器人学习的数据与工具链。

优化后的数据可面向 **多种机械臂与训练框架** 使用，并强调 **标准化与可复现** 的工程形态。（具体实现与流程细节随版本迭代公开，当前 README 仅作项目级说明。）

完整交互式排版与双语切换见 **[在线主页](https://joeland4.github.io/EasyUMI-Ego/)**。

---

## 背景与动机

### UMI 与「同构」门槛

经典 **UMI** 落地往往要求 **硬件同构**：**示教端手持夹爪**与**机械臂末端夹爪**在几何与机构上尽量一致，以缩小 embodiment gap。这在工程上 **成本高、流程繁琐**：一旦更换 **不同厂商/结构的夹爪** 或定制末端，就需要重复对齐与改造，**难以快速适配多种夹爪类型**。

- **UMI（Universal Manipulation Interface）**
  - 官方介绍：[umi-gripper.github.io](https://umi-gripper.github.io/)
  - 论文：[arXiv:2402.10329](https://arxiv.org/abs/2402.10329)
  - 代码：[real-stanford/universal_manipulation_interface](https://github.com/real-stanford/universal_manipulation_interface)

**图示（原始 UMI 同构要求）：** **左图** 为 **手持 UMI 夹爪** 进行 **示教 / 数据采集**；**右图** 为 **机械臂末端夹爪** 做 **策略部署**，其结构需与示教端 **基本保持一致**，以保证 **同构**（几何、相机位姿与接触形态一致），从而降低 embodiment gap。

<div align="center">
<table style="width:100%;max-width:760px;margin:12px auto;border-collapse:separate;border-spacing:14px;table-layout:fixed;">
  <tbody>
    <tr>
      <td align="center" valign="top" style="width:50%;padding:0;">
        <p align="center" style="margin:0 0 8px 0;"><sub><b>示教采集（手持 UMI 夹爪）</b></sub></p>
        <img src="./Visualization/left.png" alt="手持 UMI 夹爪数据采集" style="width:100%;max-width:360px;display:block;margin:0 auto;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
      </td>
      <td align="center" valign="top" style="width:50%;padding:0;">
        <p align="center" style="margin:0 0 8px 0;"><sub><b>真机部署（与示教端匹配的夹爪）</b></sub></p>
        <img src="./Visualization/right.png" alt="与 UMI 示教同构的机械臂夹爪" style="width:100%;max-width:360px;display:block;margin:0 auto;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
      </td>
    </tr>
  </tbody>
</table>
</div>

### 开源 Ego 数据、轨迹精度与 EgoMimic

开源 **第一人称 / 可穿戴（Ego）** 数据便于堆规模，但在 **轨迹可视化** 与机器人坐标系对齐后，往往暴露 **几何精度有限** 的问题，**难以较准确地直接迁移到某一固定本体**。

- **EgoMimic**
  - 项目页：[egomimic.github.io](https://egomimic.github.io/)
  - 论文：[arXiv:2410.24221](https://arxiv.org/abs/2410.24221)

**EgoMimic** 表明：仍需 **额外采集与对齐数据**，在 **Ego 手臂轨迹** 与 **单一目标机械臂** 之间做弥合，才能支撑可部署策略。

<div align="center">
<p align="center" style="max-width:560px;margin:12px auto 0;">
  <img src="./Visualization/EGO_sample.png" alt="开源 Ego 数据集轨迹可视化" style="width:100%;max-width:560px;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
</p>
</div>

### Gen-1 时代的 scaling：数量之外，更要质量

随着 **Gen-1** 等具身基础模型在 **纯 Ego 数据** 上展现出清晰的 **scaling law**，Ego 数据建设不能只追求 **条数/时长**——**对齐精度、接触与位姿可信度、与目标本体的 embodiment 一致性** 等 **数据质量** 维度，应与规模 **同等重要**。

---

## 可视化演示

> 以下为 **UMI（夹爪 + Phone）** 与 **Ego（胸口相机 + Phone）** 至 **SO101** 的示意动图。仿真、LeRobot 可视化等更多片段见 [在线主页](https://joeland4.github.io/EasyUMI-Ego/)。

<p align="center"><strong>UMI → SO101</strong></p>

<div align="center">
<table align="center" style="width:100%;max-width:520px;margin-left:auto;margin-right:auto;border-collapse:separate;border-spacing:0 16px;">
  <tbody>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>采集</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/UMIdevice.gif" alt="UMI acquisition" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>位姿 / 坐标</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/UMIpose.gif" alt="UMI pose" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>真机</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/UMIreal.gif" alt="UMI real robot" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
  </tbody>
</table>
</div>

<p align="center"><strong>Ego → SO101</strong></p>

<div align="center">
<table align="center" style="width:100%;max-width:520px;margin-left:auto;margin-right:auto;border-collapse:separate;border-spacing:0 16px;">
  <tbody>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>采集</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/EGOdevice.gif" alt="Ego acquisition" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>位姿 / 坐标</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/EGOpose.gif" alt="Ego pose" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>真机</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/EGOreal.gif" alt="Ego real robot" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
  </tbody>
</table>
</div>

---

## 核心方向

| 方向 | 说明 |
|------|------|
| **双路线覆盖** | 同时关注 **UMI** 与 **EGO** 范式，支持异构对齐与统一呈现 |
| **通用与迁移** | 弱化对单一机型或单一栈的绑定，便于扩展与复用 |
| **成本与可及性** | 优先采用 **消费级设备** 与轻量工程路径，降低准入门槛 |
| **生态对接** | 面向常见机器人学习与仿真工具链，便于后续接入训练与评估 |

---

## 项目优势

- **低成本**：无需依赖昂贵专用采集平台，适合科研与原型验证  
- **高通用**：同一套思路可覆盖多类机械臂与任务设定  
- **标准化**：强调数据与工程结构的规范性，便于协作与复现  
- **易浏览**：提供静态主页与可视化素材，方便快速了解项目定位  
- **易协作**：流程与代码组织面向团队扩展与社区反馈  

---

## 适用场景

- 具身智能 **模仿学习（Imitation Learning）**  
- 机械臂 **策略训练** 与数据准备  
- **LeRobot** 等开源机器人学习生态相关实验  
- **低成本、规模化** 机器人数据采集与试点  
- 多机型 **数据迁移与泛化** 方向的探索  

---

## 开源与许可

本项目 **完全开源**，旨在降低具身智能数据采集与实验门槛，推动机器人学习相关研究与工程应用。

- 许可证：**[MIT License](./LICENSE)**  
- 欢迎 Issue / PR 交流与改进建议  

---

**EasyUMI-Ego** — 异构对齐 UMI & Ego-centric 数据采集与展示。
