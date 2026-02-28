<h1 align="center">Hey, I'm Dhruv 👋</h1>
<h3 align="center">I write C++ and think about render pipelines more than I probably should</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/dhruv-rajvansh/"><img src="https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin" alt="LinkedIn"/></a>
  <a href="https://dhruv5262.github.io/"><img src="https://img.shields.io/badge/Portfolio-222?style=flat&logo=githubpages" alt="Portfolio"/></a>
  <a href="mailto:rajvansh@usc.edu"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

---

## About Me

I'm a CS grad student at USC Viterbi wrapping up my Master's in May 2026. My focus is pretty deep in the graphics and game engine space — C++, GPU programming, real-time systems.

I spent a lot of this past year doing two things: building a GPU particle physics engine to really understand what CUDA kernel design does to performance (spoiler: kernel fusion matters more than memory layout alone), and extending PrimeEngine with frustum culling, LOD pipelines, and skeletal animation systems from scratch.

Right now I TA for CSCI 522 (Game Engine Development) and Applied Neural Networks at USC. Graduating May 2026, looking for full-time roles in graphics, XR, or high-performance C++ systems. F-1 OPT eligible.

---

## What I Work With

**Languages:** C++ · C# · Python · Java · JavaScript/TypeScript · SQL (PostgreSQL, MySQL) · NoSQL (MongoDB) · HTML5 · GLSL · CUDA

**Frameworks & Technologies:** Unity · Unreal Engine · Three.js · WebXR API · OpenGL · Vulkan · DirectX 11 · WebGL · .NET Core · ASP.NET

**Tools & DevOps:** Git/GitHub · Perforce · Visual Studio · VS Code · AWS · Azure · Docker · Postman · GitHub Actions

**CS Fundamentals:** Multithreading · Real-time Systems · Distributed Systems · Performance Optimization · System Design · Data Structures & Algorithms

---

## Projects I'm Most Proud Of

### GPU Particle Simulation — C++/CUDA

I ran the same physics simulation (gravity + spring force + Euler integration) 5 different ways to actually measure what makes GPU code fast vs slow. CPU baseline, naive AoS GPU, SoA unfused, SoA fused, and auto-tuned block sizes.

The result that surprised me most: SoA unfused was *slower* than the naive AoS approach at 400K particles (20ms vs 14ms). Splitting into two kernels forced an extra global memory round-trip that wiped out the coalescing gains. Fusing fixed it — down to 11ms. Auto-tuning got it to 9.6ms.

At 1K particles the CPU (0.75ms) still beats the GPU (1.05ms) because kernel launch overhead dominates. That's the kind of thing you only learn by actually measuring.

**[View Repo](https://github.com/DHRUV5262/-GPU-Accelerated-Particle-Simulation-with-CPU-baseline)**

---

### PrimeEngine: Culling, LOD, Animation — C++/DirectX 12

Extended a real game engine (PrimeEngine, used in USC's CSCI 522 course) with CPU-side AABB frustum culling, a data-driven LOD pipeline using Python meta-files and Lua scripting, and distance-based animation throttling.

The frustum culling went from constant crashes at 100+ mesh instances to a stable 60 FPS. The animation work taught me why you can't just skip bone updates — the GPU shader expects a valid matrix at every index, so skipping a bone corrupts geometry downstream.

---

### Meta Quest 3 VR/MR — USC ICT (C#/Unity)

Ported legacy virtual human systems to Quest 3 using Meta's All-in-One SDK. Rebuilt the passthrough integration, locomotion system, and animation controllers. Also added speech and emotion recognition so the virtual humans could respond dynamically during training simulations.

---

### WebXR — Three.js/WebGL

Browser-based XR app using Three.js and the WebXR API. Runs in-browser, no headset required for basic interaction.

**[View Repo](https://github.com/DHRUV5262/WebXR)**

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=DHRUV5262&show_icons=true&theme=dark&hide_border=true" width="48%"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=DHRUV5262&layout=compact&theme=dark&hide_border=true" width="48%"/>
</p>

---

<p align="center">Always down to talk C++, shaders, or GPU internals. <a href="https://www.linkedin.com/in/dhruv-rajvansh/">Find me on LinkedIn</a></p>
