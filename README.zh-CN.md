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

> 以下为 **UMI（夹爪 + Phone）** 与 **Ego（胸口相机 + Phone）** 至 **SO101** 的示意动图，文件在 [`Visualization/`](./Visualization/)。仿真、LeRobot 可视化等更多片段见 [在线主页](https://joeland4.github.io/EasyUMI-Ego/)。

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
