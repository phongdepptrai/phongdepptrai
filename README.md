<div align="center">

# 💫 Hi, I'm Phong!

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=F75C7E&center=true&vCenter=true&width=500&lines=Full-Stack+Developer;AI+%26+Computer+Vision+Enthusiast;Game+Developer;OS+%26+Systems+Programmer)](https://git.io/typing-svg)

</div>

---

## 🧑‍💻 About Me

- 🎓 Student at **University of Engineering and Technology (UET)**
- 🔬 Researching **SAT/MaxSAT-based approaches to Combinatorial Optimization** — specifically the *Simple Assembly Line Balancing Problem with Power Peak Minimization* (SALB-3PM)
- 💡 Passionate about **Algorithms, AI, Computer Vision, and Systems Programming**
- 🌱 Currently exploring **Operating Systems & Security**
- ⚡ I build things ranging from SAT solvers to web tools to kernels!

---

## 🛠️ Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

</div>

---

## 🚀 Projects

### 🌐 Web & Tools

| Project | Description | Tech |
|---------|-------------|------|
| [📅 Xep-TKB-UET](https://github.com/phongdepptrai/Xep-TKB-UET) | Schedule planner tool for UET students | HTML |
| [🏠 KTXMeTri](https://github.com/phongdepptrai/KTXMeTri) | Dormitory geometry/metric tool | HTML |
| [🏠 KTXMeTri2](https://github.com/phongdepptrai/KTXMeTri2) | Dormitory metric tool v2 | HTML |
| [❤️ Heart Animation](https://github.com/phongdepptrai/phongdepptrai/blob/main/first.html) | Interactive canvas heart animation | HTML / JS |

### 🔬 Research — SAT-based Assembly Line Balancing

> **Problem:** *Simple Assembly Line Balancing with Power Peak Minimization* (SALB-3PM)
> Given *n* tasks (each with an execution time *t_i* and power draw *w_i*), *m* workstations, a cycle time *c*, and a precedence graph, assign every task to a workstation so that cycle-time and precedence constraints are satisfied while **minimising the peak simultaneous power consumption** across all workstations.
> All three repos encode this NP-hard problem as SAT / MaxSAT and solve it with state-of-the-art solvers (CaDiCaL, Glucose4, open-WBO). Benchmarks come from the classic ALB literature: MERTENS, BOWMAN, JAESCHKE, JACKSON, MANSOOR, MITCHELL, ROSZIEG, BUXEY, SAWYER, GUNTHER, WARNECKE, HESKIA.

| Project | What it does |
|---------|--------------|
| [🏭 SAML3P](https://github.com/phongdepptrai/SAML3P) | **Foundational SAT solver suite.** Introduces a novel *staircase CNF encoding* for the task-assignment (X) and start-time (S) variables, ensuring "exactly one workstation" and "consecutive activity" constraints with minimal clause overhead. Contains multiple iterative solver variants: pure staircase, pseudo-boolean (PBEnc/binmerge), incremental SAT with progressive bound tightening, and CaDiCaL-based versions. Outputs HTML Gantt-style schedule visualizations. |
| [🔧 P3SAML3P](https://github.com/phongdepptrai/P3SAML3P) | **Modular multi-solver comparison platform.** Packages six independent solver strategies — *Base*, *Staircase-1-3* (CardNet cardinality encoding), *AtmostK* (at-most-k constraint encoding), *Incremental* (progressive peak-bound tightening), *Inheritant* (warm-starting from a looser bound), and *MaxSAT* (RC2/WCNF) — behind a unified runner (`run_launcher.py`). Parametrised by `r_max` (cycle repetitions) and `R_max` (resource cap). Includes `validate_schedule.py` for correctness checking and `generate_table.py` which renders interactive HTML result tables with gap-to-lower-bound (%LB), CPU time, feasibility rate, and optimality rate. |
| [📐 MaxSatSALB3PM](https://github.com/phongdepptrai/MaxSatSALB3PM) | **Standalone MaxSAT formulation.** Encodes the peak-minimisation objective directly as a *Weighted CNF* (WCNF) formula: hard clauses enforce task assignment, precedence, and cycle-time feasibility; soft clauses penalise each unit of peak power. Solved via the *open-WBO-inc* (Glucose 4.1) incremental MaxSAT solver. Based on the paper *"Optimizing Power Peaks in Simple Assembly Line Balancing through Maximum Satisfiability"*. |

### 🤖 AI & Computer Vision

| Project | Description | Tech |
|---------|-------------|------|
| [👁️ Eyes Closed Detector](https://github.com/phongdepptrai/eyes_closed_detecter) | Drowsiness detection via eye closure | Python |
| [🧩 Block Blast Solver](https://github.com/phongdepptrai/Block_Blast_solver) | AI solver for Block Blast puzzle | Python |

### 🎮 Games

| Project | Description | Tech |
|---------|-------------|------|
| [🎯 Akarnoid-Rebond](https://github.com/phongdepptrai/Akarnoid-rebond) | Arkanoid-style bouncing game | Java |
| [🕹️ Testgame](https://github.com/phongdepptrai/Testgame) | Experimental game project | C |

### 🔐 Systems & Security

| Project | Description | Tech |
|---------|-------------|------|
| [🖥️ Aero-OS](https://github.com/phongdepptrai/Aero-OS) | Security-focused microkernel OS with biometric authentication | C |
| [🔒 ECHOVAULT](https://github.com/phongdepptrai/ECHOVAULT) | Vault / secure storage project | Java |

---

## 📊 GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=phongdepptrai&show_icons=true&theme=radical&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=phongdepptrai&layout=compact&theme=radical&hide_border=true)

![GitHub Streak](https://streak-stats.demolab.com?user=phongdepptrai&theme=radical&hide_border=true)

</div>

---

## 🌐 Connect With Me

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-phongdepptrai-181717?style=for-the-badge&logo=github)](https://github.com/phongdepptrai)

</div>

---

<div align="center">

*Made with ❤️ by phongdepptrai*

</div>
