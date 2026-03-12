<div align="center">

# 💫 Hi, I'm Phong!

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=F75C7E&center=true&vCenter=true&width=540&lines=SAT+%26+Optimization+Researcher;Full-Stack+Developer;AI+%26+Computer+Vision+Enthusiast;Game+Developer;OS+%26+Systems+Programmer)](https://github.com/DenverCoder1/readme-typing-svg)

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

> **Problem domain: SALB-3PM** — *Simple Assembly Line Balancing with Power Peak Minimization*
>
> Given *n* tasks (each with execution time *t_i* and power draw *w_i*), *m* workstations, cycle time *c*, and a precedence DAG, assign every task to exactly one workstation so that (i) the total execution time per workstation does not exceed *c*, (ii) all precedence constraints are respected, and (iii) the **peak simultaneous power draw** across all workstations and all time slots is minimized.
>
> This is an NP-hard combinatorial optimization problem. All three repositories encode it as SAT / MaxSAT and solve it with state-of-the-art solvers (**CaDiCaL 1.9.5**, **Glucose 4**, **open-WBO-inc**). Benchmark instances are drawn from the classic ALB literature: *MERTENS, BOWMAN, JAESCHKE, JACKSON, MANSOOR, MITCHELL, ROSZIEG, BUXEY, SAWYER, GUNTHER, WARNECKE, HESKIA*.

<br>

#### [🏭 SAML3P](https://github.com/phongdepptrai/SAML3P) — Foundational SAT solver suite

**Core idea:** *staircase CNF encoding* — boolean activity variables A[task][time] are encoded as a run of 1s followed by 0s (a staircase shape), with clauses enforcing each transition.

- **Feasibility:** task-assignment (X), start-time (S), and activity (A) variables encoded in CNF; solved by **CaDiCaL 1.9.5** or **Glucose 4**
- **Optimization:** ladder-variable technique — auxiliary chain U[LB+1..UB−1] where asserting ¬U[v] forces peak < v, guiding the solver from the first feasible peak down to the optimum
- **Variants:** 15+ solver configurations — pure staircase, **PBEnc/binmerge** pseudo-boolean encoding, incremental SAT with progressive peak cuts, CaDiCaL-incremental, combined PB-staircase
- **Output:** interactive HTML Gantt-style schedule visualizations per instance

---

#### [🔧 P3SAML3P](https://github.com/phongdepptrai/P3SAML3P) — Modular multi-solver comparison platform

**Extends SAML3P with two extra parameters:** `r_max` (cycle replications — horizon = `c × r_max`) and `R_max` (per-slot resource cap enforced via PBEnc cardinality).

Six solver strategies behind a unified `run_launcher.py`:

| Strategy | Description |
|----------|-------------|
| *Base* | Plain staircase feasibility |
| *Staircase-1-3* | CardNet cardinality encoding |
| *AtmostK* | At-most-k PB constraint |
| *Incremental* | Ladder-variable peak tightening (PBEnc/binmerge) |
| *Inheritant* | Warm-starts UB from a prior run at r_max−1 or R_max−1 (reads `summary.csv`) |
| *MaxSAT* | RC2/WCNF via PySAT |

`generate_table.py` renders HTML result tables (CPU time, %LB gap, feasibility %, optimality % per (r_max, R_max) pair). `validate_schedule.py` verifies every output solution.

---

#### [📐 MaxSatSALB3PM](https://github.com/phongdepptrai/MaxSatSALB3PM) — Standalone MaxSAT formulation

**Based on the paper:** *"Optimizing Power Peaks in Simple Assembly Line Balancing through Maximum Satisfiability"*

- **Hard clauses:** task assignment uniqueness, staircase activity, precedence ordering, cycle-time feasibility
- **Soft clauses:** one unit of peak power per clause (cost = 1 per violated bound)
- **Solver:** incremental *open-WBO-inc* (Glucose 4.1 static binary)
- **Results:** BUXEY → peak 315 in 472 s; HESKIA → peak 229 in 2,204 s

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
