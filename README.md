<p align="center">
  <a href="https://wavy-hec.github.io/PortfolioWebsite/">
    <img src="https://raw.githubusercontent.com/Wavy-Hec/Wavy-Hec/main/assets/terminal-header.svg" width="100%" alt="Hector Lugo III — terminal banner"/>
  </a>
</p>

<p align="center">
  <a href="https://wavy-hec.github.io/PortfolioWebsite/">
    <img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-wavy--hec.github.io-FF6F00?logo=githubpages&logoColor=white">
  </a>
  <a href="mailto:hlugo576@gmail.com">
    <img alt="Email" src="https://img.shields.io/badge/Email-hlugo576%40gmail.com-red?logo=gmail&logoColor=white">
  </a>
  <a href="https://linkedin.com/in/hector-lugo-3rd">
    <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-hector--lugo--3rd-0A66C2?logo=linkedin&logoColor=white">
  </a>
  <a href="https://github.com/Wavy-Hec">
    <img alt="GitHub" src="https://img.shields.io/badge/GitHub-Wavy--Hec-181717?logo=github&logoColor=white">
  </a>
  <a href="https://scholar.google.com/citations?user=Z-sAdqMAAAAJ&hl=en">
    <img alt="Google Scholar" src="https://img.shields.io/badge/Google%20Scholar-4285F4?logo=googlescholar&logoColor=white">
  </a>
</p>

<p align="center">
  <a href="https://wavy-hec.github.io/PortfolioWebsite/">
    <img alt="Visit My Portfolio" src="https://img.shields.io/badge/Visit_My_Portfolio-1E90FF?style=for-the-badge&logo=googlechrome&logoColor=white">
  </a>
  <a href="https://wavy-hec.github.io/PortfolioWebsite/Hector_Lugo_Resume_Spring_2026.pdf">
    <img alt="Resume" src="https://img.shields.io/badge/View_Resume-EE4C2C?style=for-the-badge&logo=adobeacrobatreader&logoColor=white">
  </a>
</p>

```python
env   = UTRGV(program="M.S. Computer Science")
agent = Hector(focus=["reinforcement learning", "robot locomotion", "VLMs"])

obs, done = env.reset(), False
while not done:                      # ← you are here
    action = agent.policy(obs)       # train robots · read papers · teach · repeat
    obs, reward, done, _ = env.step(action)
```

---

## >>> agent.whoami()

I'm Hector, a CS master's student at **UTRGV**. I mostly work on getting legged robots to move — reinforcement-learning policies trained in **NVIDIA Isaac Sim / Isaac Lab**, with the real goal being sim-to-real.

Right now I'm focused on **quadruped navigation** and **vision-language models**: an instruction goes in, the robot reads its surroundings, and (ideally) it goes where you asked. At **AFRL** I'm on the perception end of that — how VLMs handle many camera feeds at once.

<p align="center">
  <img src="https://raw.githubusercontent.com/Wavy-Hec/Wavy-Hec/main/1000056194.JPG" width="600" alt="Hector hiking in the mountains"/>
</p>

## >>> off_policy()

When I'm not training agents, I train myself: **Taekwondo** 🥋 and **hiking** 🥾, slowly working up to summiting a real mountain 🏔️.

---

## >>> observation          # current state

- 🛰️ **AI/ML Research Intern — Air Force Research Laboratory** (2026–present): multi-camera perception with vision-language models.
- 🎓 **M.S. Computer Science — UTRGV**: reinforcement learning for locomotion and multi-agent systems.
- 🧠 **Machine Intelligence Lab @ UTRGV** — [miutrgv.github.io](https://miutrgv.github.io/): RL & robotics research.
- 👨‍🏫 **Co-instructing CSCI 1101** (Intro to Computer Science) with [@jerwng](https://github.com/jerwng).
- 🔬 **Previously ML Engineer — Idaho National Laboratory** (2025–2026): ResNet autoencoders for signal denoising, cut training time by ~93%.

---

## >>> action_space         # things I reach for

<table>
  <tr>
    <td><b>Languages</b></td>
    <td>
      <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" />
      <img src="https://img.shields.io/badge/C++-00599C?logo=c%2B%2B&logoColor=white" />
      <img src="https://img.shields.io/badge/Java-007396?logo=java&logoColor=white" />
      <img src="https://img.shields.io/badge/SQL-336791?logo=postgresql&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td><b>ML / DL</b></td>
    <td>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white" />
      <img src="https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white" />
      <img src="https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white" />
      <img src="https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td><b>Robotics &amp; Sim</b></td>
    <td>
      <img src="https://img.shields.io/badge/Isaac%20Lab-000?logo=nvidia&logoColor=76B900" />
      <img src="https://img.shields.io/badge/Isaac%20Sim-000?logo=nvidia&logoColor=76B900" />
      <img src="https://img.shields.io/badge/ROS-22314E?logo=ros&logoColor=white" />
      <img src="https://img.shields.io/badge/MuJoCo-FF6B00?logo=google&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td><b>Infra &amp; Tools</b></td>
    <td>
      <img src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white" />
      <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" />
      <img src="https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black" />
      <img src="https://img.shields.io/badge/Slurm-2D4F8E?logo=gnu&logoColor=white" />
    </td>
  </tr>
</table>

---

## >>> reward               # work that landed

<table>
  <tr>
    <td>🤖</td>
    <td><b>Vision–Language Guided Quadruped Navigation with Reinforcement Learning Control</b><br/>
    <sub><i>IEEE International Conference on Machine Learning and Applications (ICMLA)</i> · 2026 · <b>accepted</b></sub></td>
  </tr>
  <tr>
    <td>📄</td>
    <td><b>Offline Reinforcement Learning Approaches for Safe and Effective Smart Grid Control</b><br/>
    <sub><i>International Congress on Information &amp; Communication Technology</i> · 2025</sub></td>
  </tr>
  <tr>
    <td>📄</td>
    <td><b>Personalized Chemotherapy Dosing Through Offline Reinforcement Learning</b><br/>
    <sub><i>International Congress on Information &amp; Communication Technology</i> · 2025</sub></td>
  </tr>
  <tr>
    <td>📄</td>
    <td><b>Spectral Clustering in Railway Crossing Accidents Analysis</b><br/>
    <sub><i>ASME/IEEE Joint Rail Conference</i> · 2024</sub></td>
  </tr>
</table>

<sub>📚 Full list &amp; citations on <a href="https://scholar.google.com/citations?user=Z-sAdqMAAAAJ&hl=en">Google Scholar</a></sub>

---

## >>> trajectory           # selected rollouts

**🤖 Robotics &amp; Reinforcement Learning**

| Project | What it does | Stack |
|---------|--------------|-------|
| **[RL_IsaacLab](https://github.com/Wavy-Hec/RL_IsaacLab)** | Multi-agent legged locomotion in simulation | Isaac Lab · LocoMuJoCo |
| **[KissICP](https://github.com/Wavy-Hec/KissICP)** | LiDAR odometry via point-to-point ICP | Python |
| **[Chess-AlphaGO](https://github.com/Wavy-Hec/Chess-AlphaGO)** | AlphaGo-style self-play agent for chess | Python |

**👁️ Computer Vision &amp; Vision-Language**

| Project | What it does | Stack |
|---------|--------------|-------|
| **[VLM](https://github.com/Wavy-Hec/VLM)** | Vision-language models for agent instruction-following | Python · PyTorch |
| **[ObjectDetection](https://github.com/Wavy-Hec/ObjectDetection)** | Real-time YOLO object detection for robotics | Python · YOLO |

**📡 Signal &amp; ML**

| Project | What it does | Stack |
|---------|--------------|-------|
| **[FFT-Denoising](https://github.com/IdahoLabUnsupported/FFT-Denoising)** | ResNet autoencoder for smart-grid signal denoising | PyTorch |

<p align="center">
  <a href="https://wavy-hec.github.io/PortfolioWebsite/"><b>→ See all projects on my portfolio</b></a>
</p>

---

## >>> tensorboard --logdir ./runs

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=Wavy-Hec&show_icons=true&theme=react&hide_border=true&count_private=true" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Wavy-Hec&layout=compact&theme=react&hide_border=true&langs_count=8" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Wavy-Hec/Wavy-Hec/main/profile-3d-contrib/profile-night-green.svg" width="100%" alt="3D isometric contribution calendar"/>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Wavy-Hec/Wavy-Hec/output/snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Wavy-Hec/Wavy-Hec/output/snake.svg" />
    <img alt="github-snake" src="https://raw.githubusercontent.com/Wavy-Hec/Wavy-Hec/output/snake.svg" />
  </picture>
</p>

---

## >>> env.step("say hi")

<p align="center">
  <i>Open to research collaborations and ML / robotics roles.</i><br/><br/>
  📫 <a href="mailto:hlugo576@gmail.com">hlugo576@gmail.com</a>
  &nbsp;·&nbsp; 🌐 <a href="https://wavy-hec.github.io/PortfolioWebsite/">Portfolio</a>
  &nbsp;·&nbsp; 💼 <a href="https://linkedin.com/in/hector-lugo-3rd">LinkedIn</a>
  &nbsp;·&nbsp; 🎓 <a href="https://scholar.google.com/citations?user=Z-sAdqMAAAAJ&hl=en">Scholar</a>
</p>

<p align="center"><sub><code>done = True  # episode complete — thanks for watching the rollout 👋</code></sub></p>
