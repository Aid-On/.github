<!-- Language Selector -->
<div align="center">

[English](README.md) | [日本語](README.ja.md)

</div>

![image](https://github.com/user-attachments/assets/dee7188a-9a10-4599-b5b3-8a8aa3968e5e)

![image](https://github.com/user-attachments/assets/0599ebde-4d33-4766-9593-4531b958ad7f)

---

# Aid-On Inc.

Aid-On is a small company in Miyazaki, Japan. We work on one thing: **the boundary of the permissions a person hands to an AI**.
Our main product, [teastia](https://aid-on.org/product), is written in
[Almide](https://github.com/almide/almide), our own language, the one an LLM writes most accurately.
It reads the source of an AI business application without running it and decides whether the application
may go to production, judged against [WASI](https://wasi.dev/) capability-based security.

The ground is WebAssembly and WASI. Enforcement is left to [Wasmtime](https://wasmtime.dev/) and the OS kernel.

> **A permission you did not grant cannot be exercised.**

Hand over only the data and the operations that are needed. Stop anything beyond that.
Take the permission back when you have to. Putting that between people and AI is what Aid-On does.

---

- Website - <https://aid-on.org/>
- Articles - <https://aid-on.org/module>
- Contact - <info@aid-on.org>

## Aid-On commercial products

- [teastia](https://aid-on.org/product) - pre-production review for AI business applications (in preparation)
- [Text Smash](https://textsmash.aid-on.org/) - read a long document by its key points, beside the original
- [Fact Judge](https://factjudge.aid-on.org/) - break a text into claims and check each one against sources
- [Spider5000](https://spider5000.aid-on.org/) - a map that grows outward from one central question

For teastia, please reach us at [info@aid-on.org](mailto:info@aid-on.org).

## Open source

### Almide

A statically typed language built so an LLM writes it accurately. It compiles to Rust and WebAssembly,
and is developed by Aid-On.

- [almide](https://github.com/almide/almide) - the compiler
- [als](https://github.com/almide/als) - the language specification, its conformance corpus, and the judge that runs it against any almide binary
- [playground](https://github.com/almide/playground) - write and run `.almd` in the browser
- [vscode-almide](https://github.com/almide/vscode-almide) / [tree-sitter-almide](https://github.com/almide/tree-sitter-almide) - editor support
- [almide-grammar](https://github.com/almide/almide-grammar) - the single source of truth for the grammar
- [parsegen](https://github.com/almide/parsegen) - a tree-sitter compatible parser generator that reads grammar.json, with no C and running in WASM
  - the parser side is to hand over to [gramide](https://github.com/O6lvl4/gramide), written in Almide, in time
- [almide-agents](https://github.com/almide/almide-agents) - an AGENTS.md that teaches a coding agent to write Almide correctly
- Organization - <https://github.com/almide>

### Porta

A sandbox that runs an agent with the permissions you actually granted it.
The limits are enforced by the OS kernel rather than by a wrapper or a prompt: Seatbelt on macOS,
Landlock and seccomp on Linux. A restriction the kernel cannot express refuses the run instead of weakening it.

- [porta](https://github.com/almide/porta)

### Libraries

- For Almide - [toml](https://github.com/Aid-On/toml) / [yaml](https://github.com/Aid-On/yaml) / [sha1](https://github.com/Aid-On/sha1)
- For TypeScript and the edge - [unillm](https://github.com/Aid-On/unillm) / [nagare](https://github.com/Aid-On/nagare) / [auth](https://github.com/Aid-On/auth) / [whenm](https://github.com/Aid-On/whenm)

The rest is in [Repositories](https://github.com/orgs/Aid-On/repositories).
Each repository carries its own LICENSE.

## About us

| | |
| --- | --- |
| **Mission** | A world where people and AI can safely entrust their strengths to each other |
| **Vision** | Making it ordinary to take on challenges together with AI |
| **Value** | Trust opens possibilities |

More at <https://aid-on.org/>.

## Company

|                |                            |
| -------------- | -------------------------- |
| **Company Name** | Aid-On Inc. / 株式会社 Aid-On |
| **Location**   | Miyazaki City, Miyazaki Prefecture, Japan |
| **Business**   | Planning, development, consulting, and maintenance of artificial intelligence and applied technology software and systems |
| **Contact**    | [info@aid-on.org](mailto:info@aid-on.org) |

---

© 2026 Aid-On Inc.
