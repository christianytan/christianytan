<!--
  Profile README — this renders on https://github.com/christianytan
  It only works from a repository named exactly `christianytan`.
-->

<h1 align="center">Christian Tan</h1>

<p align="center">
  <strong>Japanese–English Bilingual IT Professional</strong> · <strong>JLPT N3</strong><br>
  <sub>Rust · TypeScript · Flutter — small systems that stay correct, and tools that make Japanese learnable.</sub>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/christiantanjp"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/christianytan"><img src="https://img.shields.io/badge/GitHub-christianytan-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>
  <img src="https://img.shields.io/badge/Based_in-Japan-BC002D?style=flat-square" alt="Based in Japan">
  <img src="https://img.shields.io/badge/JLPT-N3-2E7D32?style=flat-square" alt="JLPT N3">
  <img src="https://komarev.com/ghpvc/?username=christianytan&style=flat-square&color=2088ff" alt="Profile views">
</p>

<br>

```text
♟️  chess engines in Rust        →  fenex · fenpix · small-uci · cirno-chess-engine
🈺  Japanese learning tools      →  hokengo · jlpt kanji dataset · kanji SRS app
🦀  systems & data tooling       →  registry_cleaner · OctQuant · UniQuant · BatchReencode
🤖  Discord bots (Touhou-named)  →  alice_bot · bread_bot · kogasa-bot
🏠  self-hosted LLM inference    →  4× Tesla P100 · 64 GB VRAM · nothing leaves the house
```

## About

I work professionally in two languages — Japanese and English — and most of what I build exists because the tooling I wanted as a Japanese learner wasn't there.

- **Libraries over apps.** I like small, dependency-light crates that do one thing correctly, published where people can actually use them — [`fenex` and `fenpix` on crates.io](https://crates.io/crates/fenpix), [`small-uci` on npm](https://www.npmjs.com/package/small-uci).
- **Local-first by default.** No account, no server, no telemetry — progress lives on the device, with a plain-file export so nothing is ever trapped.
- **Typed and tested.** Rust for anything that has to stay correct, TypeScript with strict types and Vitest for the UI, GitHub Actions for typecheck → test → build → deploy.
- **Currently:** expanding `hokengo`'s insurance-IT vocabulary set, and building `registry_cleaner` — a tool for the Windows uninstall entries that refuse to go away.

---

## Selected work

### 🈺 [hokengo](https://github.com/christianytan/hokengo) — 保険・IT 用語トレーナー

<a href="https://christianytan.github.io/hokengo/"><img src="https://img.shields.io/badge/Live_demo-2088FF?style=flat-square&logo=githubpages&logoColor=white" alt="Live demo"></a>
<img src="https://img.shields.io/github/languages/top/christianytan/hokengo?style=flat-square" alt="Language">

A browser-based vocabulary trainer for Japanese insurance terminology and the IT vocabulary around it, aimed at learners around JLPT N3–N2 who work with Japanese insurers or insurance IT. Five question modes, self-graded spaced repetition, kana readings for terms *and* full example sentences, browser read-aloud, an offline service worker, and JSON backup/restore. Everything is stored in IndexedDB — there is no server and no telemetry.

### ♟️ [fenex](https://github.com/christianytan/fenex) · [fenpix](https://github.com/christianytan/fenpix) — published on crates.io

<a href="https://crates.io/crates/fenex"><img src="https://img.shields.io/crates/v/fenex?style=flat-square" alt="fenex on crates.io"></a>
<a href="https://crates.io/crates/fenpix"><img src="https://img.shields.io/crates/v/fenpix?style=flat-square" alt="fenpix on crates.io"></a>
<a href="https://crates.io/crates/fenpix"><img src="https://img.shields.io/crates/d/fenpix?style=flat-square" alt="fenpix downloads"></a>

**fenex** is the foundation: an efficient 8×8 board model with full rule implementation, FEN parsing and algebraic-coordinate conversion, plus a modular API for applying moves and simulating positions — the piece I kept rewriting in every chess project. It also runs in the browser through [fenex_wasm_api](https://christianytan.github.io/fenex_wasm_api/).
**fenpix** renders a FEN string straight into a pixel-art board image using hand-made sprites, with automatic orientation, asset preloading and scaling, exporting to file or memory.

### 📚 [jlpt_kanji_json_msgpack](https://github.com/christianytan/jlpt_kanji_json_msgpack) — most-starred

<a href="https://github.com/christianytan/jlpt_kanji_json_msgpack"><img src="https://img.shields.io/github/stars/christianytan/jlpt_kanji_json_msgpack?style=flat-square&logo=github" alt="stars"></a>

Kanji for JLPT N5–N1 only, filtered out of the 13,000-entry kanjiapi.dev dataset and shipped as both JSON and MessagePack: **93.5 MB → 0.5 MB**, a 99.5% reduction, so a learning app can load the whole dictionary onto the device and look up a kanji in one hash access.

### 🏠 Home AI inference server — self-hosted

<img src="https://img.shields.io/badge/4%C3%97_Tesla_P100-64_GB_VRAM-0071B5?style=flat-square&logo=nvidia&logoColor=white" alt="4x Tesla P100, 64 GB VRAM">
<img src="https://img.shields.io/badge/self_hosted-no_API_bill-2E7D32?style=flat-square" alt="self-hosted">

Four NVIDIA Tesla P100 GPUs (64 GB VRAM total) serving quantized LLMs locally — Hermes and OpenClaw-based coding models — through LM Studio and Unsloth Studio. Multi-GPU model loading for low-latency inference and long-context experimentation, used for day-to-day programming assistance and prompt testing. No API bill, and no prompt leaves the machine.

### 📱 Kanji SRS app — Flutter / Dart

A spaced-repetition kanji trainer with custom HTML/CSS components, covering the full study flow: review sessions, progress tracking and card scheduling. Built alongside the dataset above; the Play Store listing is pending production.

---

## Elsewhere in the workshop

| Project | What it does |
|---|---|
| [registry_cleaner](https://github.com/christianytan/registry_cleaner) | 🦀 Finds the ghost entries in Windows **Apps & Features** — the ones where you press Uninstall and nothing happens because the app is already gone. Reads every Add/Remove Programs key, checks what it points at on disk, sorts by confidence. Nothing is removed without asking. |
| [small-uci](https://github.com/christianytan/small-uci) | 🔠 A deliberately small UCI interface for talking to chess engines — on [npm](https://www.npmjs.com/package/small-uci) |
| [poorcraft](https://github.com/christianytan/poorcraft) | 🧱 A deliberately poor imitation of Minecraft: a blocky voxel world you can walk, mine and build in. Plain HTML + Three.js, no build step, runs offline. |
| [BatchReencode](https://github.com/christianytan/BatchReencode) | 🐍 Browse a local video library, queue batch re-encodes, monitor progress — the tool behind my anime re-encode pipeline |
| [OctQuant](https://github.com/christianytan/OctQuant) · [UniQuant](https://github.com/christianytan/UniQuant) | 🎨 Octree and uniform image quantization in Go, GIF and PNG |
| [qwen3.8-flash-next-iq3_s benchmark](https://github.com/christianytan/qwen3.8-flash-next-iq3_s-pagoda-benchmark) | 📊 Quantization benchmark results for a Qwen3 build, published on GitHub Pages |
| [danbooru-tag-collector](https://github.com/christianytan/danbooru-tag-collector) | 🏷️ The complete Danbooru tag list as CSV, plus the collector that pulled it |
| [cirno-chess-engine](https://github.com/christianytan/cirno-chess-engine) | ♟️ The first attempt at a real engine, before `fenex` existed |
| [alice_bot](https://github.com/christianytan/alice_bot) · [bread_bot](https://github.com/christianytan/bread_bot) · [kogasa-bot](https://github.com/christianytan/kogasa-bot) | 🤖 Discord bots in Rust and TypeScript — every one of them named after a Touhou character |
| [VoiceVoxEngToJpn](https://github.com/christianytan/VoiceVoxEngToJpn) | 🗣️ English → Japanese speech through VOICEVOX |
| [privacy_policies](https://github.com/christianytan/privacy_policies) | 🔒 The privacy policy pages for my apps, static on GitHub Pages |


## How I work

- If a tool annoys me twice, I write the tool — then publish it so the annoyance only happens once.
- A library should be readable in ten minutes. `small-uci` and `fenex` are named that way on purpose.
- Offline is a feature, not a fallback. Several of my projects are built to run with the network switched off.
- Data a user generates belongs on the user's device, and it must be exportable as a plain file.
- Bilingual is more than translating strings: `hokengo` ships kana readings and example sentences, because that is what a learner actually needs.

<!--
  Optional stats cards. Uncomment this block to enable them.
  They are served by a third-party service, so they can rate-limit or load slowly;
  the README renders perfectly well without them.

| | |
|---|---|
| <img src="https://github-readme-stats.vercel.app/api?username=christianytan&show_icons=true&count_private=true&hide_title=true&theme=gruvbox" alt="GitHub stats"> | <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=christianytan&layout=compact&hide_title=true&theme=gruvbox" alt="Top languages"> |
-->

---

## Contact

<p align="center">
  <a href="https://www.linkedin.com/in/christiantanjp"><img src="https://img.shields.io/badge/LinkedIn-christiantanjp-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/christianytan"><img src="https://img.shields.io/badge/GitHub-christianytan-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
</p>

<p align="center"><sub>LinkedIn is the fastest way to reach me. My email stays off the public internet on purpose.</sub></p>
