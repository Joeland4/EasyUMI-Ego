# EasyUMI-Ego

[English](README.md) · **简体中文**

**具身智能数据采集优化框架** — 面向 **UMI** 与 **EGO（第一人称 / 可穿戴）** 两类主流具身数据采集与对齐场景，配套静态项目主页（[`index.html`](./index.html) + [`Visualization/`](./Visualization/)）便于展示与分享。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Pages](https://img.shields.io/badge/GitHub-Pages-222?logo=github)](https://joeland4.github.io/EasyUMI-Ego/)

---

## 目录

- [项目简介](#项目简介)
- [可视化演示](#可视化演示)
- [核心方向](#核心方向)
- [项目优势](#项目优势)
- [适用场景](#适用场景)
- [开源与许可](#开源与许可)

---

## 项目简介

本项目围绕 **UMI** 与 **EGO** 两条具身智能数据路线，在 **采集成本**、**机械臂适配** 与 **数据可用性** 等方向做系统化优化，便于在消费级硬件条件下获得可用于机器人学习的数据与工具链。

优化后的数据可面向 **多种机械臂与训练框架** 使用，并强调 **标准化与可复现** 的工程形态。（具体实现与流程细节随版本迭代公开，当前 README 仅作项目级说明。）

完整交互式排版与双语切换见 **[在线主页](https://joeland4.github.io/EasyUMI-Ego/)**（[`index.html`](./index.html)）。

---

## 可视化演示

> 以下为 **UMI（夹爪 + Phone → SO101）** 示意动图，文件在 [`Visualization/`](./Visualization/)。**Ego 路线**及其它片段见 [在线主页](https://joeland4.github.io/EasyUMI-Ego/)。为控制版面，此处以较小尺寸展示；需要看清细节可在仓库中打开原 GIF 或访问主页全屏查看。

<p align="center"><strong>UMI → SO101</strong></p>

<table align="center" style="width:100%;max-width:720px;table-layout:fixed;border-collapse:separate;border-spacing:10px;">
  <tr>
    <td style="width:33.33%;vertical-align:top;text-align:center;padding:0;">
      <sub><b>采集</b></sub><br/><br/>
      <img src="./Visualization/UMIdevice.gif" alt="UMI acquisition" style="width:100%;height:200px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
    </td>
    <td style="width:33.33%;vertical-align:top;text-align:center;padding:0;">
      <sub><b>位姿 / 坐标</b></sub><br/><br/>
      <img src="./Visualization/UMIpose.gif" alt="UMI pose" style="width:100%;height:200px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
    </td>
    <td style="width:33.33%;vertical-align:top;text-align:center;padding:0;">
      <sub><b>真机</b></sub><br/><br/>
      <img src="./Visualization/UMIreal.gif" alt="UMI real robot" style="width:100%;height:200px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
    </td>
  </tr>
</table>

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
