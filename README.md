# Mohamed Amin MAKNI

**AI Engineer · Software Engineer** — Sfax, Tunisia

I build systems that have to be right in operation, not only in evaluation.

That distinction is most of what I do. A detector that scores 95% mAP@50 and a document pipeline a business can run on are different achievements, and the gap between them is where the engineering lives: confidence thresholds, human review paths, business rules, and tests for the parts that decide whether the system can be trusted.

National Engineering Degree in Computer Engineering, International Institute of Technology — graduated 18 July 2026.

## Selected work

### [Fytrak](https://github.com/medaminmakni/Fytrak) — coaching platform *(personal project, built solo)*

A three-role platform — trainee, coach, administrator — built end to end: React Native app, admin web console, and fifteen Cloud Functions covering the coach-assignment lifecycle, write-time aggregation, scheduled reporting and a subscription webhook. English, French and Arabic including right-to-left.

The part I would want reviewed first is the access model: 698 lines of Firestore security rules with an explicit role model, and a test suite that runs them against the emulator. An access rule nobody has tested is an assumption, not a rule.

Deliberately no AI in V1 — the product needed a direct line between a coach and their client, and a model in that path would have added latency and a failure mode to a problem messaging already solved.

### ORYS — AI layer *(team of four, in progress)*

I am responsible for the model and agent layer of a multi-tenant business platform.

A provider abstraction with two adapters behind one interface — OpenAI-compatible, serving Ollama, OpenAI and OpenRouter, and one for the Anthropic Messages API — so changing provider is configuration rather than code. Both adapters derive their wire formats from the vendors' published SDK types rather than from documentation, which surfaced three defects every existing test had passed; two would have reached production.

Agent tools each wrap exactly one API call made as the acting user. The agent holds no database credential and never sees SQL, so every action inherits that user's permissions and audit trail.

### [SmartWarehouse AI](https://github.com/medaminmakni/smartWareHouse)

A logistics agent deciding gate assignment from plate recognition, separating facts (SQL) from rules (vector retrieval). I built a retrieval evaluation for it and found the two policy documents driving its decisions were never being retrieved; fixing the embedding model and the chunking moved recall@5 from 33% to 44%.

### OptiFlow Precal Insight — Essilor SIVO (EssilorLuxottica)

Final-year engineering project: a document-intelligence pipeline combining YOLO11 field detection, EfficientNetV2-S classification, TrOCR and GLM-OCR recognition, business rules and human review. Confidential, so no code or screenshots.

## Stack

- **Machine learning** — Python, PyTorch, TensorFlow, deep learning, NumPy, pandas, scikit-learn, model evaluation
- **Computer vision** — YOLO, YOLO11, EfficientNetV2, OCR, TrOCR, object detection
- **Generative AI & NLP** — LLMs, RAG, AI agents, transformers, natural language processing, ChromaDB, vector databases, embeddings
- **Backend & cloud** — FastAPI, Node.js, NestJS, REST APIs, SQL, PostgreSQL, MySQL, MongoDB, Google Cloud (Firebase, Cloud Functions, Firestore)
- **Delivery** — Docker, Linux, Git, CI/CD, Agile/Scrum, unit testing, TypeScript, Next.js, React, React Native

## Certifications

- Information Technology Specialist — Artificial Intelligence · Certiport · 889/1000 · Oct 2024
- Information Technology Specialist — Python · Certiport · 880/1000 · Mar 2024
- Hashgraph Developer · The Hashgraph Association · Jun 2025

## Writing

I keep engineering notes on [my portfolio](https://med-amin-makni.vercel.app/notes) — most recently on why an AI agent should never confirm its own high-risk action, and on why mAP@50 is not a promise.

## Elsewhere

[Portfolio](https://med-amin-makni.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/makni-med-amin/) · [mki.medamin@gmail.com](mailto:mki.medamin@gmail.com)

*Open to AI Engineer roles — Tunisia, remote, or with relocation. Available immediately.*
