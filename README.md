# EasyUMI-Ego

**English** · [简体中文](README.zh-CN.md)

**Embodied intelligence data collection framework** — optimizing **UMI** and **egocentric (wearable)** capture–to–alignment workflows, with a static project page ([`index.html`](./index.html) + [`Visualization/`](./Visualization/)) for sharing.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Pages](https://img.shields.io/badge/GitHub-Pages-222?logo=github)](https://joeland4.github.io/EasyUMI-Ego/)

---

## Contents

- [Overview](#overview)
- [Visual demos](#visual-demos)
- [Focus areas](#focus-areas)
- [Highlights](#highlights)
- [Use cases](#use-cases)
- [License](#license)

---

## Overview

This project improves two embodied data routes — **UMI** and **EGO** — across **cost**, **robot compatibility**, and **data usability**, so useful robot-learning data and tooling are reachable on **consumer-grade hardware**.

Outputs aim to support **multiple robot arms and training stacks** with a **standardized, reproducible** engineering story. (Implementation details are released over time; this README stays at the project level.)

For the full interactive layout and language toggle, open the **[live site](https://joeland4.github.io/EasyUMI-Ego/)** or [`index.html`](./index.html).

---

## Visual demos

> **UMI** and **Ego (chest-mounted phone → SO101)** preview GIFs are in [`Visualization/`](./Visualization/). More clips (simulation, LeRobot vis, etc.) are on the [live site](https://joeland4.github.io/EasyUMI-Ego/).

<p align="center"><strong>UMI → SO101</strong></p>

<div align="center">
<table align="center" style="width:100%;max-width:520px;margin-left:auto;margin-right:auto;border-collapse:separate;border-spacing:0 16px;">
  <tbody>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>Acquisition</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/UMIdevice.gif" alt="UMI acquisition" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>Pose / coordinates</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/UMIpose.gif" alt="UMI pose" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>Real robot</b></sub></p>
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
        <p align="center" style="margin:0;"><sub><b>Acquisition</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/EGOdevice.gif" alt="Ego acquisition" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>Pose / coordinates</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/EGOpose.gif" alt="Ego pose" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
    <tr>
      <td align="center" style="padding:0;text-align:center;">
        <p align="center" style="margin:0;"><sub><b>Real robot</b></sub></p>
        <p align="center" style="margin:12px 0 0 0;max-width:520px;margin-left:auto;margin-right:auto;">
          <img src="./Visualization/EGOreal.gif" alt="Ego real robot" style="width:100%;height:220px;object-fit:cover;object-position:center;display:block;border-radius:8px;border:1px solid #e0e0e0;box-sizing:border-box;"/>
        </p>
      </td>
    </tr>
  </tbody>
</table>
</div>

---

## Focus areas

| Area | Description |
|------|-------------|
| **Dual pipelines** | Covers **UMI** and **EGO** styles with heterogeneous alignment and a unified presentation |
| **Generalization** | Less tied to one arm or one stack — easier to extend and reuse |
| **Cost & access** | Favors **consumer devices** and lightweight engineering paths |
| **Ecosystem fit** | Plays well with common robot-learning and simulation tooling |

---

## Highlights

- **Low cost** — no reliance on expensive bespoke capture rigs; good for research and prototypes  
- **Broad applicability** — one mindset can cover many arms and task setups  
- **Standardization** — clear structure for collaboration and reproduction  
- **Easy to skim** — static page + visuals for quick orientation  
- **Collaboration-friendly** — layout and code organized for teams and community input  

---

## Use cases

- Embodied **imitation learning**  
- Manipulator **policy training** and data prep  
- Experiments in open stacks such as **LeRobot**  
- **Low-cost, larger-scale** robot data pilots  
- **Cross-arm transfer and generalization** explorations  

---

## License

Fully **open source** — to lower the barrier to embodied data collection and robot-learning work.

- **License:** [MIT License](./LICENSE)  
- Issues and PRs welcome  

---

**EasyUMI-Ego** — heterogeneous alignment for UMI & egocentric capture and presentation.
