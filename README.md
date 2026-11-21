# Hi, I'm Vaibhav Gupta

I build **LLM agent systems** and make **large models run on small hardware**. My focus is on the engineering that makes AI features reliable: validation, human approval, undo, tests and honest measurement.

Open to freelance projects.

## Selected work

| Project | What it shows |
|---|---|
| [**quorum**](https://github.com/vaibhavgupta443/quorum) | An agent that turns meeting transcripts into verified tasks and calendar events. The model records *what was said*; plain code replays it, so the final plan is deterministic and testable. MCP server, human approval step, evals. |
| [**clout**](https://github.com/vaibhavgupta443/clout) | A social-media life simulation with LLM-backed characters: memory and reflection, a Director that only *proposes* until you approve, exact undo, a live SillyTavern bridge, hybrid retrieval. About 30k lines of JavaScript and 100+ test files. Built with a documented Claude Code multi-agent workflow. |
| [**local-diffusion-4gb**](https://github.com/vaibhavgupta443/local-diffusion-4gb) | Getting current image models to run in 8-30 s on a 4 GB GPU with 7.4 GB RAM: custom quantisation, pruning a text encoder, a bit-identical prompt cache, and fixes for a VAE quality bug and a CUDA crash. Measured, with dead ends written down. |
| [**changelens**](https://github.com/vaibhavgupta443/changelens) | An AI assistant for pull-request review (React, Spring Boot, FastAPI). Early stage: the three-service skeleton runs, review logic is next. The README says exactly what is and is not built. |

## How I work

- **Measure first.** On a memory-starved laptop the bottleneck was RAM, not the GPU. I find that out before optimising.
- **Models propose, code decides.** Output is validated before it changes anything, and risky actions wait for a person.
- **Say what is verified and what is not.** My write-ups separate measured results from third-party claims and guesses.
- **Small steps with cheap checks**, so problems show up in seconds, not at the end.

## Tools

Python · JavaScript · Java (Spring Boot) · React · FastAPI · SQLite · ComfyUI · PyTorch · llama.cpp · Claude Code
