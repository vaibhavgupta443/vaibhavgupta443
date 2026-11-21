<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=170&section=header&text=Vaibhav%20Gupta&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=AI%20engineer%20%C2%B7%20LLM%20agents%20%C2%B7%20efficient%20local%20models&descSize=17&descAlignY=60" alt="Vaibhav Gupta, AI engineer" />

<a href="https://github.com/vaibhavgupta443/clout">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=620&height=40&lines=LLM+agent+systems+that+stay+reliable;Big+models+on+small+GPUs%2C+measured+honestly;Human+approval%2C+undo%2C+and+real+tests" alt="Typing animation" />
</a>

<br/>

<a href="https://github.com/vaibhavgupta443?tab=followers"><img src="https://img.shields.io/github/followers/vaibhavgupta443?style=for-the-badge&logo=github&color=203a43" alt="followers" /></a>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />

</div>

---

## About

I build **LLM agent systems** and make **large models run on small hardware**. What I care about is the engineering that makes AI features trustworthy: validation, human approval, undo, tests, and measurements I can defend.

**Quick links:** [Projects](#projects) · [Highlights](#highlights) · [How I work](#how-i-work) · [Tech](#tech)

---

## Projects

<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/vaibhavgupta443/quorum">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=quorum&theme=tokyonight&hide_border=true" alt="quorum" />
      </a>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/vaibhavgupta443/clout">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=clout&theme=tokyonight&hide_border=true" alt="clout" />
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/vaibhavgupta443/local-diffusion-4gb">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=local-diffusion-4gb&theme=tokyonight&hide_border=true" alt="local-diffusion-4gb" />
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/vaibhavgupta443/changelens">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=changelens&theme=tokyonight&hide_border=true" alt="changelens" />
      </a>
    </td>
  </tr>
</table>

<details>
<summary><b>What each one demonstrates</b> (click to expand)</summary>

<br/>

| Project | What it shows |
|---|---|
| **[quorum](https://github.com/vaibhavgupta443/quorum)** | An agent that turns meeting transcripts into verified tasks and calendar events. The model records *what was said*; plain code replays it, so the final plan is deterministic and testable. MCP server, a human approval step, evals. |
| **[clout](https://github.com/vaibhavgupta443/clout)** | A social-media life simulation with LLM-backed characters: memory and reflection, a Director that only *proposes* until you approve, exact undo, a live SillyTavern bridge, hybrid retrieval. About 30k lines of JavaScript and 100+ test files, built with a documented Claude Code multi-agent workflow. |
| **[local-diffusion-4gb](https://github.com/vaibhavgupta443/local-diffusion-4gb)** | Getting current image models to run in 8-30 s on a 4 GB GPU with 7.4 GB RAM: custom quantisation, pruning a text encoder, a bit-identical prompt cache, and fixes for a VAE quality bug and a CUDA crash. Measured, with the dead ends written down. |
| **[changelens](https://github.com/vaibhavgupta443/changelens)** | An AI assistant for pull-request review (React, Spring Boot, FastAPI). Early stage: the three-service skeleton runs and review logic is next. The README states exactly what is and is not built. |

</details>

---

## Highlights

<details>
<summary><b>Optimisation: a text encoder that was 29% dead weight</b></summary>

<br/>

FLUX.2 Klein 9B reads only layers 9, 18 and 27 of its Qwen3-8B text encoder, so layers 27-35, the final norm and the LM head can be removed. The catch: the final norm must also be disabled, or the last tap comes out normalised and wrong. Details and the ComfyUI node are in [local-diffusion-4gb](https://github.com/vaibhavgupta443/local-diffusion-4gb/blob/main/docs/03-text-encoder.md).

</details>

<details>
<summary><b>Debugging: edits that burned out, and a crash on every second job</b></summary>

<br/>

A tiled VAE decode compounded error across chained image edits; a whole-image decode fixed the drift and was faster (32 s to 21 s). Separately, leftover CUDA cache collided with dynamic VRAM and crashed every second job; a small pass-through node fixed it without reloading the model. Write-ups: [editing quality](https://github.com/vaibhavgupta443/local-diffusion-4gb/blob/main/docs/05-editing-quality.md) and [memory and offloading](https://github.com/vaibhavgupta443/local-diffusion-4gb/blob/main/docs/04-memory-and-offloading.md).

</details>

<details>
<summary><b>Agent design: the model proposes, code decides</b></summary>

<br/>

In both [quorum](https://github.com/vaibhavgupta443/quorum) and [clout](https://github.com/vaibhavgupta443/clout), model output is validated before it changes anything, risky actions wait for a person, and every action can be undone. See the [architecture notes](https://github.com/vaibhavgupta443/clout/blob/main/docs/ARCHITECTURE.md).

</details>

---

## How I work

- **Measure first.** On a memory-starved laptop the bottleneck was RAM, not the GPU. I find that out before optimising.
- **Models propose, code decides.** Output is validated, and risky actions wait for a person.
- **Say what is verified and what is not.** My write-ups separate what I measured from third-party claims and guesses.
- **Small steps with cheap checks**, so problems show up in seconds, not at the end.

---

## Tech

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,js,java,spring,react,fastapi,sqlite,pytorch,nodejs,git,github&perline=11" alt="Tech stack" />
</p>

<p align="center"><sub>Also: ComfyUI · llama.cpp · Claude Code · MCP</sub></p>

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=vaibhavgupta443&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" alt="Top languages" />
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=90&section=footer" alt="" width="100%" />
