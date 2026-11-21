<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=170&section=header&text=Vaibhav%20Gupta&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=Java%20%C2%B7%20Spring%20Boot%20%C2%B7%20backend%20engineering%20%C2%B7%20AI%20tooling&descSize=17&descAlignY=60" alt="Vaibhav Gupta, Java and Spring Boot developer" />

<a href="https://github.com/vaibhavgupta443/changelens">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&height=40&lines=Java+and+Spring+Boot+backends;Static+analysis+and+developer+tooling;LLM+features+that+are+checked%2C+not+trusted" alt="Typing animation" />
</a>

<br/>

<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
<img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />

</div>

---

## About

I am a Java developer. I build backend services with **Spring Boot** (REST, JPA, Spring Security with JWT), and I like developer tooling: tools that read code and make engineers' work clearer. I also build features around LLMs, with the rule that model output is validated and checkable, never simply trusted.

**Quick links:** [Featured](#featured-projects) · [Highlights](#highlights) · [Tech](#tech)

---

## Featured projects

<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/vaibhavgupta443/changelens">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=changelens&theme=tokyonight&hide_border=true&v=20261121" alt="changelens" />
      </a>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/vaibhavgupta443/quorum">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=quorum&theme=tokyonight&hide_border=true&v=20261121" alt="quorum" />
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/vaibhavgupta443/syncup">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=syncup&theme=tokyonight&hide_border=true&v=20261121" alt="syncup" />
      </a>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/vaibhavgupta443/lowvram-diffusion-lab">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=vaibhavgupta443&repo=lowvram-diffusion-lab&theme=tokyonight&hide_border=true&v=20261121" alt="lowvram-diffusion-lab" />
      </a>
    </td>
  </tr>
</table>

<details>
<summary><b>What each one shows</b> (click to expand)</summary>

<br/>

| Project | Stack | What it shows | Where to see it |
|---|---|---|---|
| **[changelens](https://github.com/vaibhavgupta443/changelens)** | Java 21, Spring Boot, JavaParser, JGit, Maven, GitHub Actions; Python (experimental AI service) | Reads a pull request with a real Java parser and tells the reviewer what changed at package, class and method level, what behaviour is new, and which endpoints run through the change. Measured on a labelled evaluation set, with the limits written down. | [Live PR comment](https://github.com/vaibhavgupta443/changelens/pull/1) · [Releases](https://github.com/vaibhavgupta443/changelens/releases) · use it: `uses: vaibhavgupta443/changelens@v0.1.2` |
| **[quorum](https://github.com/vaibhavgupta443/quorum)** | Python, FastAPI, MCP, Google Calendar API, pytest | An agent that turns meeting transcripts into verified tasks and calendar events. The model records *what was said*; plain code replays it, so the result is deterministic and testable. Human approval step, evals. | Runs locally (setup in the README) |
| **[syncup](https://github.com/vaibhavgupta443/syncup)** | Java, Spring Boot 3, MySQL, JWT; React 19, Vite; Docker | Full-stack activity and social-matching platform. | [Live app](https://syncup-eta.vercel.app) |
| **[lowvram-diffusion-lab](https://github.com/vaibhavgupta443/lowvram-diffusion-lab)** | Python, PyTorch, ComfyUI nodes | **Research.** Notes, measurements and ComfyUI nodes from running current image models on a 4 GB GPU with 7.4 GB of RAM: quantisation, pruning, caching, two bug fixes. | [Write-ups](https://github.com/vaibhavgupta443/lowvram-diffusion-lab/tree/main/docs) |

</details>

---

## Highlights

<details>
<summary><b>Engineering approach</b></summary>

<br/>

- **Measure first.** On a memory-starved laptop the bottleneck turned out to be RAM, not the GPU ([write-up](https://github.com/vaibhavgupta443/lowvram-diffusion-lab/blob/main/docs/01-where-the-time-goes.md)).
- **Facts from code, language from models.** In quorum and ChangeLens the model never decides what is true; code does.
- **Say what is verified and what is not.** Limits are written next to the results.

</details>

---

## Tech

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,maven,postgres,mysql,python,react,git,github,githubactions&perline=11" alt="Tech stack" />
</p>

<p align="center"><sub>Also: Quarkus · JPA/Hibernate · JWT · JUnit · FastAPI · JavaParser · Node.js</sub></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=90&section=footer" alt="" width="100%" />
